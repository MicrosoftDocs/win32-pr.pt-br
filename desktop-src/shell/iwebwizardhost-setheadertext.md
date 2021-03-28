---
description: Define o título e o subtítulo que aparecem no cabeçalho do assistente. Em geral, o cliente exibirá o cabeçalho acima do HTML e abaixo da barra de título.
title: Método WebWizardHost. setheadertext (shldisp. h)
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
ms.openlocfilehash: 92e23fab94cfedd8bbc62e31086759af48238a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968076"
---
# <a name="webwizardhostsetheadertext-method"></a>Método WebWizardHost. setheadertext

Define o título e o subtítulo que aparecem no cabeçalho do assistente. Em geral, o cliente exibirá o cabeçalho acima do HTML e abaixo da barra de título.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrHeaderTitle* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadeia de caracteres que contém o título.

</dd> <dt>

*bstrHeaderSubtitle* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadeia de caracteres que contém o subtítulo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 
