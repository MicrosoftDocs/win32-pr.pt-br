---
description: Navega até a página do lado do cliente imediatamente antes da página que hospeda as páginas HTML do lado do servidor.
title: Método WebWizardHost. FinalBack (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: f131050bb5dd4cfc4b8533857c306f566f12ec2d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841867"
---
# <a name="webwizardhostfinalback-method"></a>Método WebWizardHost. FinalBack

Navega até a página do lado do cliente imediatamente antes da página que hospeda as páginas HTML do lado do servidor.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="remarks"></a>Comentários

Quando o assistente exibe a primeira página do lado do servidor e o usuário clica no botão **voltar** , o servidor invoca **FinalBack** quando notificado sobre esse evento pelo manipulador de eventos do cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




