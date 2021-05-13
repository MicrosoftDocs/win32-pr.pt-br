---
description: Navega até a página do assistente do lado do cliente que segue a página que hospeda as páginas HTML do lado do servidor ou termina o assistente se não houver mais páginas do lado do cliente.
title: Método WebWizardHost.FinalNext (Shldisp.h)
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
ms.openlocfilehash: fa59a70c04e7f78a315955aeabb9477c6f28c80d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841837"
---
# <a name="webwizardhostfinalnext-method"></a>Método WebWizardHost.FinalNext

Navega até a página do assistente do lado do cliente que segue a página que hospeda as páginas HTML do lado do servidor ou termina o assistente se não houver mais páginas do lado do cliente.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="remarks"></a>Comentários

Quando o assistente estiver exibindo a última página HTML  do  lado do servidor e o usuário clicar no botão Próximo ou Concluir, o servidor invocará **FinalNext** no manipulador de eventos desse botão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente \[ aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Somente aplicativos da área de trabalho do Windows Server 2003 \[\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




