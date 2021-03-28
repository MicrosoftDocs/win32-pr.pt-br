---
description: Navega até a página do assistente do lado do cliente que segue a página que hospeda as páginas HTML do lado do servidor ou conclui o assistente se não houver outras páginas do lado do cliente.
title: Método WebWizardHost. FinalNext (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: 5693de342b03a9ee4b7ed04cf24d8cfa9ee8b784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170477"
---
# <a name="webwizardhostfinalnext-method"></a>Método WebWizardHost. FinalNext

Navega até a página do assistente do lado do cliente que segue a página que hospeda as páginas HTML do lado do servidor ou conclui o assistente se não houver outras páginas do lado do cliente.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="remarks"></a>Comentários

Quando o assistente estiver exibindo a última página HTML do lado do servidor e o usuário clicar no botão **Avançar** ou **concluir** , o servidor invocará **FinalNext** no manipulador de eventos desse botão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




