---
title: Tratamento de erro COM em Java e Visual Basic
description: Tratamento de erro COM em Java e Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c55c1c2414c69ff9398845858baadebd58cbf9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424006"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a>Tratamento de erro COM em Java e Visual Basic

Há três interfaces e três funções que podem ser usadas em COM para fornecer tratamento de erros durante a programação em Java ou Microsoft Visual Basic. Em Java e Visual Basic, a chamada de método não retorna um **HRESULT** como o valor de retorno. Em vez disso, esses idiomas usam as interfaces e funções COM para obter valores **HRESULT** e para tratar erros ou exceções. (Exceções são eventos além do controle do programa, como problemas de arquivo ou parâmetros inválidos.)

As três interfaces que fornecem suporte para **HRESULT** s são listadas e descritas brevemente na tabela a seguir.



|  Interface                                                                        |  Descrição                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | Define informações de erro.<br/>                                                                                   |
| [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | Retorna informações de um objeto de erro.<br/>                                                                 |
| [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | Identifica o objeto como suporte à interface [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .<br/> |



 

As três funções que fornecem suporte para **HRESULT** s são listadas e descritas brevemente na tabela a seguir.



|    Interface       |       Descrição       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | Cria uma instância de um objeto de erro genérico.<br/>                                                                                                            |
| [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | Obtém o ponteiro de informações de erro definido pela chamada anterior para [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) no thread lógico atual.<br/> |
| [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | Define o objeto de informações de erro para o thread atual de execução.<br/>                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erro em COM](error-handling-in-com.md)
</dt> </dl>

 

