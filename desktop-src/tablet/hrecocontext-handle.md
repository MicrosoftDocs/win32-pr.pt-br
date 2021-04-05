---
description: Um identificador HRECOCONTEXT é usado para adicionar tinta ao contexto, executar o reconhecimento de tinta (de forma síncrona ou assíncrona), recuperar o resultado do reconhecimento e recuperar alternativas.
ms.assetid: 509188e2-28af-4915-bc76-ee451133398f
title: Identificador HRECOCONTEXT (recapitular. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13ef2b6f629587de84f831fd32a31f42a208c024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827197"
---
# <a name="hrecocontext-handle"></a>Identificador de HRECOCONTEXT

Um identificador **HRECOCONTEXT** é usado para adicionar tinta ao contexto, executar o reconhecimento de tinta (de forma síncrona ou assíncrona), recuperar o resultado do reconhecimento e recuperar alternativas.

O principal motivo para os identificadores de contexto do reconhecedor é diferenciar as entradas de tinta. Por exemplo, você pode criar um aplicativo com duas janelas, o usuário sendo capaz de fazer a tinta em qualquer uma das janelas. Você não quer ter a tinta da primeira janela misturada com a tinta da segunda janela quando solicita que o reconhecedor reconheça a tinta de uma das janelas. Nesse tipo de aplicativo, você cria dois contextos de reconhecedor (um para cada janela) e adiciona traços que entram na janela 1 no contexto 1 do reconhecedor e traços da janela 2 no contexto do reconhecedor 2. Para retornar os resultados de reconhecimento, chame o processo no contexto do reconhecedor 1 ou no contexto 2 do reconhecedor, dependendo se você deseja os resultados para a janela 1 ou 2.

O identificador de contexto do reconhecedor pode ser qualquer coisa que você desejar. Mas, normalmente, é um índice em uma matriz global de estruturas. As estruturas podem conter todos os traços que foram inseridos e todas as variáveis que o reconhecedor usa para aquela parte de tinta específica (por exemplo, sua estrutura malha interna ou o estado atual de reconhecimento). Uma estrutura pode conter todas as informações que o reconhecedor precisa e usa para uma determinada parte da tinta.

Para obter um identificador **HRECOCONTEXT** , chame a função [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) .


```C++
typedef HANDLE HRECOCONTEXT;
```



## <a name="remarks"></a>Comentários

A seguir estão as funções **HRECOCONTEXT**



| Função                                                            | Descrição                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addstroke**](/windows/desktop/api/recapis/nf-recapis-addstroke)                                      | Adiciona um traço de tinta ao contexto do reconhecedor.<br/>                                                                                                                                                                                                    |
| [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange)                          | Impede que o reconhecedor processe a tinta porque um novo traço está sendo adicionado ou excluído.<br/>                                                                                                                                                         |
| [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext)                                | Cria um contexto de reconhecedor que contém as mesmas configurações que o original. O novo contexto do reconhecedor não inclui os resultados de tinta ou de reconhecimento do original.<br/>                                                                        |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)             | Indica que nenhuma tinta será adicionada ao contexto.<br/>                                                                                                                                                                                         |
| [**Getalternativolist**](/previous-versions/windows/desktop/legacy/ms698163(v=vs.85))                        | Retorna uma lista de alternativas para a melhor cadeia de caracteres de resultado.<br/>                                                                                                                                                                                         |
| [**GetBestAlternate**](/previous-versions/windows/desktop/legacy/ms699575(v=vs.85))                        | Retorna um ponteiro de [identificador HRECOALT](hrecoalt-handle.md) para a melhor alternativa de resultado.<br/>                                                                                                                                                         |
| [**GetBestResultString**](/windows/desktop/api/recapis/nf-recapis-getbestresultstring)                  | Retorna a melhor cadeia de caracteres de resultado.<br/>                                                                                                                                                                                                                  |
| [**GetContextPropertyList**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)            | Retorna uma lista de propriedades às quais o reconhecedor dá suporte.<br/>                                                                                                                                                                                            |
| [**GetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)          | Retorna um valor de propriedade especificado do contexto do reconhecedor.<br/>                                                                                                                                                                                  |
| [**GetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)          | Retorna uma lista de intervalos de pontos Unicode habilitados no contexto.<br/>                                                                                                                                                                                   |
| [**Getguia**](/windows/desktop/api/recapis/nf-recapis-getguide)                                        | Retorna o guia usado para entrada em caixa ou embutida.<br/>                                                                                                                                                                                                 |
| [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr)                              | Retorna um ponteiro para o malha para os resultados atuais.<br/>                                                                                                                                                                                        |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) | Retorna um valor que indica se uma palavra, data, hora, número ou outro texto passado está contido no dicionário.<br/>                                                                                                               |
| [**Processar**](/windows/desktop/api/recapis/nf-recapis-process)                                          | Executa o reconhecimento de tinta de forma síncrona.<br/>                                                                                                                                                                                                          |
| [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext)                                | Exclui a tinta atual e os resultados de reconhecimento do contexto.<br/>                                                                                                                                                                                |
| [**SetCACMode**](/windows/desktop/api/recapis/nf-recapis-setcacmode)                                    | Especifica o modo de preenchimento automático de caractere para reconhecimento de caracteres ou palavras.<br/>                                                                                                                                                                         |
| [**SetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)          | Adiciona uma propriedade ao contexto do reconhecedor. Se uma propriedade já existir, seu valor será modificado.<br/>                                                                                                                                                  |
| [**SetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)          | Habilita um ou mais intervalos de ponto Unicode no contexto.<br/>                                                                                                                                                                                         |
| [**Setfactoid**](/windows/desktop/api/recapis/nf-recapis-setfactoid)                                    | Define o factor que um reconhecedor usa para restringir sua pesquisa para o resultado.<br/>                                                                                                                                                                       |
| [**SetFlags**](/windows/desktop/api/recapis/nf-recapis-setflags)                                        | Define como o reconhecedor interpreta a tinta e determina a cadeia de caracteres de resultado.<br/>                                                                                                                                                                     |
| [**Guia de**](/windows/desktop/api/recapis/nf-recapis-setguide)                                        | Define o guia a ser usado para entrada em caixa ou em linha.<br/>                                                                                                                                                                                                  |
| [**SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext)                            | Fornece as cadeias de caracteres de texto que vêm antes e depois do texto contido no contexto do reconhecedor. Para reconhecedores de caracteres do leste asiático, a função [**SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext) fornece caracteres em vez de cadeias de texto.<br/> |
| [**Setwordlist**](/windows/desktop/api/recapis/nf-recapis-setwordlist)                                  | Define a lista de palavras para o contexto do reconhecedor atual reconhecer.<br/>                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Recapitular. h</dt> </dl> |



 

