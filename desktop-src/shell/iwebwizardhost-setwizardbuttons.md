---
description: Atualiza os botões voltar, avançar e concluir no quadro do assistente do cliente.
title: Método WebWizardHost. SetWizardButtons (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968075"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>Método WebWizardHost. SetWizardButtons

Atualiza os botões **voltar**, **Avançar** e **concluir** no quadro do assistente do cliente.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vbEnableBack* \[ no\]
</dt> <dd>

Tipo: **booliano**

Habilita o botão **voltar** .

</dd> <dt>

*vbEnableNext* \[ no\]
</dt> <dd>

Tipo: **booliano**

Habilita botão **Avançar**.

</dd> <dt>

*vbLastPage* \[ no\]
</dt> <dd>

Tipo: **booliano**

Habilita o botão **concluir** . Declara que esta é a última página do lado do servidor.

</dd> </dl>

## <a name="remarks"></a>Comentários

Certifique-se de implementar funções de manipulador em cada página do lado do servidor para onback () e OnNext (), correspondente aos botões do assistente de **volta** e **próximo**. As funções onback () e OnNext () respondem a **SetWizardButtons**. No momento apropriado, a função OnNext () chama **SetWizardButtons** com *vbLastPage* = **true**, que pode habilitar um botão **concluir** . OnNext () também chama [**FinalNext**](iwebwizardhost-finalnext.md) quando um usuário clica no botão **concluir** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




