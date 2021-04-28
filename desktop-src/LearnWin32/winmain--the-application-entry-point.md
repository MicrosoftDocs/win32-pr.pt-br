---
Título: WinMain a descrição do ponto de entrada do aplicativo: WinMain: o ponto de entrada do aplicativo MS. AssetID: 389da5d4-d0f9-4339-BE6C-0f4fecc59316 MS. tópico: artigo MS. Date: 05/31/2018
---

# <a name="winmain-the-application-entry-point"></a>WinMain: o ponto de entrada do aplicativo

Cada programa do Windows inclui uma função de ponto de entrada denominada **WinMain** ou **wWinMain**. Aqui está a assinatura para **wWinMain**.


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



Os quatro parâmetros são:

-   *HINSTANCE* é algo chamado "identificador para uma instância" ou "identificador para um módulo". O sistema operacional usa esse valor para identificar o executável (EXE) quando ele é carregado na memória. O identificador de instância é necessário para determinadas funções do Windows, por exemplo, para carregar ícones ou bitmaps.
-   *hPrevInstance* não tem significado. Ele foi usado no Windows de 16 bits, mas agora é sempre zero.
-   *pCmdLine* contém os argumentos de linha de comando como uma cadeia de caracteres Unicode.
-   *nCmdShow* é um sinalizador que indica se a janela principal do aplicativo será minimizada, maximizada ou exibida normalmente.

A função retorna um valor **int** . O valor de retorno não é usado pelo sistema operacional, mas você pode usar o valor de retorno para transmitir um código de status para outro programa que você escreve.

**Winapi tenha** é a Convenção de chamada. Uma *Convenção de chamada* define como uma função recebe parâmetros do chamador. Por exemplo, ele define a ordem em que os parâmetros aparecem na pilha. Apenas certifique-se de declarar sua função **wWinMain** , conforme mostrado.

A função **WinMain** é idêntica a **wWinMain**, exceto que os argumentos de linha de comando são passados como uma cadeia de caracteres ANSI. A versão Unicode é preferida. Você pode usar a função ANSI **WinMain** mesmo se compilar seu programa como Unicode. Para obter uma cópia Unicode dos argumentos de linha de comando, chame a função [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) . Essa função retorna todos os argumentos em uma única cadeia de caracteres. Se você quiser os argumentos como uma matriz de estilo *argv*, passe essa cadeia de caracteres para [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).

Como o compilador sabe invocar **wWinMain** em vez da função **Main** padrão? O que realmente acontece é que a Microsoft C Runtime Library (CRT) fornece uma implementação de **Main** que chama **WinMain** ou **wWinMain**.

> [!Note]  
> O CRT faz algum trabalho adicional dentro do **principal**. Por exemplo, todos os inicializadores estáticos são chamados antes de **wWinMain**. Embora você possa instruir o vinculador a usar uma função de ponto de entrada diferente, use o padrão se você vincular ao CRT. Caso contrário, o código de inicialização do CRT será ignorado, com resultados imprevisíveis. (Por exemplo, objetos globais não serão inicializados corretamente.)

 

Aqui está uma função **WinMain** vazia.


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



Agora que você tem o ponto de entrada e entende algumas das convenções básicas de terminologia e codificação, você está pronto para criar um programa de janela completo.

## <a name="next"></a>Avançar

[Módulo 1. Seu primeiro programa do Windows](your-first-windows-program.md).

 

 
