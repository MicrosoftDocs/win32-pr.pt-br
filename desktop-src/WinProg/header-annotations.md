---
title: Anotações de cabeçalho
description: As anotações de cabeçalho descrevem como uma função usa seus parâmetros e valor de retorno.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- API do Windows, anotações de arquivo de cabeçalho
- anotações de arquivo de cabeçalho
- Specstrings. h
- idioma de anotação padrão (SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8535118383a97d6c48f19246ad24ce324e8bb528
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105802092"
---
# <a name="header-annotations"></a>Anotações de cabeçalho

\[Este tópico descreve as anotações com suporte nos cabeçalhos do Windows por meio do Windows 7. Se você estiver desenvolvendo para o Windows 8, deverá usar as anotações descritas em [anotações sal]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]

As anotações de cabeçalho descrevem como uma função usa seus parâmetros e valor de retorno. Essas anotações foram adicionadas a muitos dos arquivos de cabeçalho do Windows para ajudá-lo a garantir que você está chamando a API do Windows corretamente. Se você habilitar a análise de código, que está disponível a partir do Visual Studio 2005, o compilador produzirá avisos de nível 6000 se você não estiver chamando essas funções de acordo com o uso descrito por meio das anotações. Você também pode adicionar essas anotações em seu próprio código para garantir que ele esteja sendo chamado corretamente. Para habilitar a análise de código no Visual Studio, consulte a documentação da sua versão do Visual Studio.

Essas anotações são definidas em Specstrings. h. Eles são criados em primitivos que fazem parte da linguagem de anotação padrão (SAL) e implementados usando o `_declspec("SAL_*")` .

Há duas classes de anotações: anotações de buffer e anotações avançadas.

## <a name="buffer-annotations"></a>Anotações de buffer

As anotações de buffer descrevem como as funções usam seus ponteiros e podem ser usadas para detectar saturações de buffer. Cada parâmetro pode usar uma anotação de buffer ou zero. Uma anotação de buffer é construída com um sublinhado à esquerda e os componentes descritos nas seções a seguir.



| Tamanho do buffer                                                                                  | Description                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_size_"></span><span id="_SIZE_"></span>(*tamanho*)<br/>                        | Especifica o tamanho total do buffer. Use with \_ bcount e \_ ecount; não use with \_ Part. Esse valor é o espaço acessível; pode ser menor do que o espaço alocado.<br/> |
| <span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*tamanho*,*comprimento*)<br/> | Especifica o tamanho total e o tamanho inicializado do buffer. Use with \_ bcount \_ Part e \_ ecount \_ Part. O tamanho total pode ser menor do que o espaço alocado.<br/>              |



 



| Unidades de tamanho do buffer                                                       | Description                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount<br/> | O tamanho do buffer está em bytes.<br/>    |
| <span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount<br/> | O tamanho do buffer está em elementos.<br/> |



 



| Direção                                                            | Descrição                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_in"></span><span id="_IN"></span>\_no<br/>          | A função lê do buffer. O chamador fornece o buffer e o inicializa.<br/>                                                                                                                          |
| <span id="_inout"></span><span id="_INOUT"></span>\_InOut<br/> | A função lê e grava no buffer. O chamador fornece o buffer e o inicializa. Se usado com \_ Deref, o buffer pode ser realocado pela função.<br/>                                      |
| <span id="_out"></span><span id="_OUT"></span>\_fora<br/>       | A função grava no buffer. Se usado no valor de retorno ou com \_ Deref, a função fornece o buffer e o inicializa. Caso contrário, o chamador fornecerá o buffer e a função o inicializará.<br/> |



 



| Indireção                                                                       | Description                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="_deref"></span><span id="_DEREF"></span>\_Deref<br/>              | Desfaça referência ao parâmetro para obter o ponteiro do buffer. Este parâmetro não pode ser **nulo**.<br/> |
| <span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_Deref \_ aceitar<br/> | Desfaça referência ao parâmetro para obter o ponteiro do buffer. Este parâmetro pode ser **NULL**.<br/>     |



 



| Inicialização                                                    | Description                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="_full"></span><span id="_FULL"></span>\_completo<br/> | A função inicializa todo o buffer. Use somente com buffers de saída.<br/>                                     |
| <span id="_part"></span><span id="_PART"></span>\_parte<br/> | A função inicializa parte do buffer e indica explicitamente o quanto. Use somente com buffers de saída.<br/> |



 



| Buffer necessário ou opcional                                    | Description                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span id="_opt"></span><span id="_OPT"></span>\_opt<br/> | Este parâmetro pode ser **NULL**.<br/> |



 

O exemplo a seguir mostra as anotações da função **GetModuleFileName** . O parâmetro *HMODULE* é um parâmetro de entrada opcional. O parâmetro *lpFileName* é um parâmetro de saída; seu tamanho em caracteres é especificado pelo parâmetro *nSize* e seu comprimento inclui o caractere de terminação **nula**. O parâmetro *nSize* é um parâmetro de entrada.


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



A seguir estão as anotações definidas em Specstrings. h. Use as informações nas tabelas acima para interpretar seu significado.

__bcount (*tamanho*)  
__bcount_opt (*tamanho*)  
__deref_bcount (*tamanho*)  
__deref_bcount_opt (*tamanho*)  
__deref_ecount (*tamanho*)  
__deref_ecount_opt (*tamanho*)  
__deref_in  
__deref_in_bcount (*tamanho*)  
__deref_in_bcount_opt (*tamanho*)  
__deref_in_ecount (*tamanho*)  
__deref_in_ecount_opt (*tamanho*)  
__deref_in_opt  
__deref_inout  
__deref_inout_bcount (*tamanho*)  
__deref_inout_bcount_full (*tamanho*)  
__deref_inout_bcount_full_opt (*tamanho*)  
__deref_inout_bcount_opt (*tamanho*)  
__deref_inout_bcount_part (*tamanho*,*comprimento*)  
__deref_inout_bcount_part_opt (*tamanho*,*comprimento*)  
__deref_inout_ecount (*tamanho*)  
__deref_inout_ecount_full (*tamanho*)  
__deref_inout_ecount_full_opt (*tamanho*)  
__deref_inout_ecount_opt (*tamanho*)  
__deref_inout_ecount_part (*tamanho*,*comprimento*)  
__deref_inout_ecount_part_opt (*tamanho*,*comprimento*)  
__deref_inout_opt  
__deref_opt_bcount (*tamanho*)  
__deref_opt_bcount_opt (*tamanho*)  
__deref_opt_ecount (*tamanho*)  
__deref_opt_ecount_opt (*tamanho*)  
__deref_opt_in  
__deref_opt_in_bcount (*tamanho*)  
__deref_opt_in_bcount_opt (*tamanho*)  
__deref_opt_in_ecount (*tamanho*)  
__deref_opt_in_ecount_opt (*tamanho*)  
__deref_opt_in_opt  
__deref_opt_inout  
__deref_opt_inout_bcount (*tamanho*)  
__deref_opt_inout_bcount_full (*tamanho*)  
__deref_opt_inout_bcount_full_opt (*tamanho*)  
__deref_opt_inout_bcount_opt (*tamanho*)  
__deref_opt_inout_bcount_part (*tamanho*,*comprimento*)  
__deref_opt_inout_bcount_part_opt (*tamanho*,*comprimento*)  
__deref_opt_inout_ecount (*tamanho*)  
__deref_opt_inout_ecount_full (*tamanho*)  
__deref_opt_inout_ecount_full_opt (*tamanho*)  
__deref_opt_inout_ecount_opt (*tamanho*)  
__deref_opt_inout_ecount_part (*tamanho*,*comprimento*)  
__deref_opt_inout_ecount_part_opt (*tamanho*,*comprimento*)  
__deref_opt_inout_opt  
__deref_opt_out  
__deref_opt_out_bcount (*tamanho*)  
__deref_opt_out_bcount_full (*tamanho*)  
__deref_opt_out_bcount_full_opt (*tamanho*)  
__deref_opt_out_bcount_opt (*tamanho*)  
__deref_opt_out_bcount_part (*tamanho*,*comprimento*)  
__deref_opt_out_bcount_part_opt (*tamanho*,*comprimento*)  
__deref_opt_out_ecount (*tamanho*)  
__deref_opt_out_ecount_full (*tamanho*)  
__deref_opt_out_ecount_full_opt (*tamanho*)  
__deref_opt_out_ecount_opt (*tamanho*)  
__deref_opt_out_ecount_part (*tamanho*,*comprimento*)  
__deref_opt_out_ecount_part_opt (*tamanho*,*comprimento*)  
__deref_opt_out_opt  
__deref_out  
__deref_out_bcount (*tamanho*)  
__deref_out_bcount_full (*tamanho*)  
__deref_out_bcount_full_opt (*tamanho*)  
__deref_out_bcount_opt (*tamanho*)  
__deref_out_bcount_part (*tamanho*,*comprimento*)  
__deref_out_bcount_part_opt (*tamanho*,*comprimento*)  
__deref_out_ecount (*tamanho*)  
__deref_out_ecount_full (*tamanho*)  
__deref_out_ecount_full_opt (*tamanho*)  
__deref_out_ecount_opt (*tamanho*)  
__deref_out_ecount_part (*tamanho*,*comprimento*)  
__deref_out_ecount_part_opt (*tamanho*,*comprimento*)  
__deref_out_opt  
__ecount (*tamanho*)  
__ecount_opt (*tamanho*)  
__in  
__in_bcount (*tamanho*)  
__in_bcount_opt (*tamanho*)  
__in_ecount (*tamanho*)  
__in_ecount_opt (*tamanho*)  
__in_opt  
__inout  
__inout_bcount (*tamanho*)  
__inout_bcount_full (*tamanho*)  
__inout_bcount_full_opt (*tamanho*)  
__inout_bcount_opt (*tamanho*)  
__inout_bcount_part (*tamanho*,*comprimento*)  
__inout_bcount_part_opt (*tamanho*,*comprimento*)  
__inout_ecount (*tamanho*)  
__inout_ecount_full (*tamanho*)  
__inout_ecount_full_opt (*tamanho*)  
__inout_ecount_opt (*tamanho*)  
__inout_ecount_part (*tamanho*,*comprimento*)  
__inout_ecount_part_opt (*tamanho*,*comprimento*)  
__inout_opt  
__out  
__out_bcount (*tamanho*)  
__out_bcount_full (*tamanho*)  
__out_bcount_full_opt (*tamanho*)  
__out_bcount_opt (*tamanho*)  
__out_bcount_part (*tamanho*,*comprimento*)  
__out_bcount_part_opt (*tamanho*,*comprimento*)  
__out_ecount (*tamanho*)  
__out_ecount_full (*tamanho*)  
__out_ecount_full_opt (*tamanho*)  
__out_ecount_opt (*tamanho*)  
__out_ecount_part (*tamanho*,*comprimento*)  
__out_ecount_part_opt (*tamanho*,*comprimento*)  
__out_opt  

## <a name="advanced-annotations"></a>Anotações avançadas

As anotações avançadas fornecem informações adicionais sobre o parâmetro ou valor de retorno. Cada parâmetro ou valor de retorno pode usar uma anotação avançada ou zero.



| Annotation                                                                                                                                               | Description                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocos (*recurso*)<br/> | As funções são bloqueadas no recurso especificado.<br/>                                                                                                                                                                                                                      |
| <span id="__callback"></span><span id="__CALLBACK"></span>\_\_retorno<br/>                                                                        | A função pode ser usada como um ponteiro de função.<br/>                                                                                                                                                                                                                      |
| <span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn<br/>                               | Os chamadores devem verificar o valor de retorno.<br/>                                                                                                                                                                                                                                 |
| <span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_Cadeia de formato \_<br/>                                                        | O parâmetro é uma cadeia de caracteres que contém marcadores de estilo printf%.<br/>                                                                                                                                                                                                      |
| <span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_em \_ awcount (*expr*,*size*)<br/>                            | Se a expressão for verdadeira na saída, o tamanho do buffer de entrada será especificado em bytes. Se a expressão for false, o tamanho será especificado em elementos.<br/>                                                                                                                |
| <span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated<br/>                                          | O buffer pode ser acessado até e incluindo a primeira sequência de dois caracteres ou ponteiros **nulos** .<br/>                                                                                                                                                            |
| <span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated<br/>                                                      | O buffer pode ser acessado até e incluindo o primeiro caractere ou ponteiro **nulo** .<br/>                                                                                                                                                                              |
| <span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount (*expr*,*size*)<br/>                         | Se a expressão for verdadeira na saída, o tamanho do buffer de saída será especificado em bytes. Se a expressão for false, o tamanho será especificado em elementos. <br/>                                                                                                              |
| <span id="__override"></span><span id="__OVERRIDE"></span>\_\_substituição<br/>                                                                        | Especifica o comportamento de substituição do estilo C# para métodos virtuais.<br/>                                                                                                                                                                                                           |
| <span id="__reserved"></span><span id="__RESERVED"></span>\_\_reservado<br/>                                                                        | O parâmetro é reservado para uso futuro e deve ser zero ou **nulo**.<br/>                                                                                                                                                                                               |
| <span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_êxito (*expr*)<br/>                                                       | Se a expressão for verdadeira na saída, o chamador poderá contar com todas as garantias especificadas por outras anotações. Se a expressão for false, o chamador não poderá contar com as garantias. Essa anotação é adicionada automaticamente a funções que retornam um valor **HRESULT** .<br/> |
| <span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)<br/>                                                    | Trate o parâmetro como o tipo especificado em vez de seu tipo declarado.<br/>                                                                                                                                                                                             |



 

Os exemplos a seguir mostram o buffer e as anotações avançadas para as funções [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)e [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) .


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Anotações de SAL](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[Walkthrough: analisando o código C/C++ para defeitos](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

