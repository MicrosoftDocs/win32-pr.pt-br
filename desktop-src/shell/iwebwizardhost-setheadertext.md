---
description: Define o título e o subtítulo que aparecem no título do assistente. Em geral, o cliente exibirá o título acima do HTML e abaixo da barra de título.
title: Método WebWizardHost.SetHeaderText (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: d524f9ae6d1031d518e237d393bbb1dc0d35b2bd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841827"
---
# <a name="webwizardhostsetheadertext-method"></a>Método WebWizardHost.SetHeaderText

Define o título e o subtítulo que aparecem no título do assistente. Em geral, o cliente exibirá o título acima do HTML e abaixo da barra de título.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrHeaderTitle* \[ Em\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadeia de caracteres que contém o título.

</dd> <dt>

*bstrHeaderSubtitle* \[ Em\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadeia de caracteres que contém o subtítulo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente \[ aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Somente aplicativos da área de trabalho do Windows Server 2003 \[\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 
