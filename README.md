import fundamentus
import pandas as pd


class analisar_multiplos():

    def __init__(self, dataframe = None, acao = None):
        
        self.df = dataframe

        self.papel = acao

    def gerar_acoes(self):

        self.df = fundamentus.get_resultado_raw().reset_index()

        print(self.df.head())

        self.df.to_html('raiz4.html')

    def filtrar_acao(self, acao):

        df = self.df

        filtro = df['papel'] == acao

        df2 = df[filtro]

        print(df2)    


raiz4 = analisar_multiplos()

raiz4.gerar_acoes()

raiz4.filtrar_acao('RAIZ4')



