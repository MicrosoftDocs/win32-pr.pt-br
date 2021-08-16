---
description: Atualiza os botões Voltar, Próximo e Concluir no quadro do assistente do cliente.
title: Método WebWizardHost.SetWizardButtons (Shldisp.h)
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
ms.openlocfilehash: 36b40d0831c18a7931f3f29492dd4c7769440a76ddcec2aa33ba3e840e97950d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859119"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>Método WebWizardHost.SetWizardButtons

Atualiza os **botões Voltar,** **Próximo** **e** Concluir no quadro do assistente do cliente.

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

*vbEnableBack* \[ Em\]
</dt> <dd>

Tipo: **booliana**

Habilita o **botão** Voltar.

</dd> <dt>

*vbEnableNext* \[ Em\]
</dt> <dd>

Tipo: **booliana**

Habilita botão **Avançar**.

</dd> <dt>

*vbLastPage* \[ Em\]
</dt> <dd>

Tipo: **booliana**

Habilita o **botão** Concluir. Declara que esta é a última página do lado do servidor.

</dd> </dl>

## <a name="remarks"></a>Comentários

Certifique-se de implementar funções de manipulador em cada página do lado do servidor para OnBack() e OnNext(), correspondentes aos botões do assistente **Voltar** e **Próximo.** As funções OnBack() e OnNext() respondem a **SetWizardButtons.** No momento apropriado, a função OnNext() chama **SetWizardButtons** com *vbLastPage* = **true,** que pode habilitar um **botão** Concluir. OnNext() também chama [**FinalNext**](iwebwizardhost-finalnext.md) quando um usuário clica no **botão** Concluir.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




