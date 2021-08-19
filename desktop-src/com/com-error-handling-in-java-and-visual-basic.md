---
title: Tratamento de erro COM em Java e Visual Basic
description: Tratamento de erro COM em Java e Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba8e179ca3e7a1d57fdae63e8ad20d14a6fff358fab1fff24bfe7ae8df185d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048514"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a>Tratamento de erro COM em Java e Visual Basic

Há três interfaces e três funções que podem ser usadas em COM para fornecer tratamento de erro ao programar em Java ou Microsoft Visual Basic. Em Java e Visual Basic, a chamada de método não retorna um **HRESULT** como o valor de retorno. Em vez disso, essas linguagens usam as interfaces e funções COM para obter **valores HRESULT** e para tratar erros ou exceções. (Exceções são eventos além do controle do programa, como problemas de arquivo ou parâmetros inválidos.)

As três interfaces que oferecem suporte para **HRESULT** s são listadas e descritas brevemente na tabela a seguir.



|  Interface                                                                        |  Descrição                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**Icreateerrorinfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | Define informações de erro.<br/>                                                                                   |
| [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | Retorna informações de um objeto de erro.<br/>                                                                 |
| [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | Identifica o objeto como dando suporte à interface [**IErrorInfo.**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/> |



 

As três funções que fornecem suporte para **HRESULT** s são listadas e descritas brevemente na tabela a seguir.



|    Interface       |       Descrição       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | Cria uma instância de um objeto de erro genérico.<br/>                                                                                                            |
| [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | Obtém o ponteiro de informações de erro definido pela chamada anterior para [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) no thread lógico atual.<br/> |
| [**Seterrorinfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | Define o objeto de informações de erro para o thread de execução atual.<br/>                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erro em COM](error-handling-in-com.md)
</dt> </dl>

 

