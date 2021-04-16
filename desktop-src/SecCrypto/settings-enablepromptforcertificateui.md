---
description: Define ou recupera um valor booliano que especifica se os prompts de interface do usuário para uma identidade de signatário ou remetente podem ser usados.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Propriedade Settings. EnablePromptForCertificateUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758157"
---
# <a name="settingsenablepromptforcertificateui-property"></a>Propriedade Settings. EnablePromptForCertificateUI

\[A propriedade **EnablePromptForCertificateUI** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]

A propriedade **EnablePromptForCertificateUI** define ou recupera um valor booliano que especifica se os prompts de interface do usuário para a identidade de um signatário ou remetente podem ser usados.

## <a name="syntax"></a>Syntax


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se **for true**, os prompts da interface do usuário para o assinante ou a identidade do remetente poderão ser usados. O valor padrão é **false**.

> [!Note]  
> Definir essa propriedade não desabilita os avisos gerados antes de qualquer uso de chave privada ser feito de um aplicativo baseado na Web.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configurações**](settings.md)
</dt> </dl>

 

 




