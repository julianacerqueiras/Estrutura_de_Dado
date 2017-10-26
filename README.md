# Estrutura_de_Dado
void pilha_imprime(Pilha* p){
     Lista* q;
     for(q = p->prim; q != NULL; q = q->prox)     
           printf("%f\n", q->info);
           
}

void imprime(Pilha* p){
     Pilha* aux = pilha_cria();
     while(!vazia(p)){
         pilha_push(aux,pilha_pop(p));
     }
     while(!vazia(aux)){
         float v = pilha_pop(aux);
         printf("%f\n", v);
         pilha_push(p,v);
     }
     pilha_libera(aux);
}
