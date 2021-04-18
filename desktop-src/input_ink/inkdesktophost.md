---
description: Implementa a interface IInkDesktopHost.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: Classe InkDesktopHost
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: d5dac80a4ee09bb4b78a4d61ca0efa74e99babb9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "105764326"
---
# <a name="inkdesktophost-class"></a>Classe InkDesktopHost

Implementa a interface [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) .

Um objeto [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) permite entrada, processamento e renderização de tinta por meio da criação de um thread de aplicativo para hospedar um objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e inseri-lo na árvore visual do [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo.

## <a name="members"></a>Membros

A classe **InkDesktopHost** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **InkDesktopHost** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **InkDesktopHost** tem esses métodos.

| Método | Descrição |
|---|---|
| [**CreateAndInitializeInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | Cria um objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) em um thread de aplicativo, conecta-o à árvore visual [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo e define o tamanho do objeto.<br/> |
| [**Createinkpresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | Cria um objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) em um thread de aplicativo.<br/> |
| [**QueueWorkItem**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | Adicione uma operação de tinta a uma fila de trabalho para execução no thread **InkDesktopHost** .<br/> |

## <a name="creationaccess-functions"></a>Criar \\ funções de acesso

Chame [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com o identificador de classe <strong>InkDesktopHost</strong> para recuperar uma referência ao objeto.

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&amp;_spInkHost));
```

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|---|---|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/> |
| parâmetro<br/>                   | <dl> <dt>InkPresenterDesktop. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>InkPresenterDesktop. idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkDesktopHost é definido como 4ce7d875-A981-4140-a1ff-ad93258e8d59<br/> |

## <a name="related-topics"></a>Tópicos relacionados

[Classes de apresentador de tinta](ink-presenter-classes.md), [interações de caneta e caneta](/windows/uwp/design/input/pen-and-stylus-interactions), [exemplo de análise de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), exemplo de [escrita simples](/samples/microsoft/windows-universal-samples/simpleink/), [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/)
