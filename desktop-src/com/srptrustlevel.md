---
title: SRPTrustLevel
description: Define o nível de confiança da política de restrição de software (SRP) para aplicativos.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- COM valor do registro SRPTrustLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363837"
---
# <a name="srptrustlevel"></a>SRPTrustLevel

Define o nível de confiança da política de restrição de software (SRP) para aplicativos.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um valor **reg \_ DWORD** que está disponível a partir do Windows XP.



| Valor                                 | Descrição                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| 0x0 (nível de segurança do cofre não \_ \_ permitido)      | O aplicativo não é permitido de acessar e de privilégios de usuário sensíveis à segurança. |
| 0x40000 ( \_ nível de \_ FULLYTRUSTED seguro) | O aplicativo tem acesso irrestrito aos privilégios do usuário.                    |



 

Se o valor de **SRPTrustLevel** não existir, \_ será usado o valor padrão de restarid de nível mais seguro \_ . Se **SRPTrustLevel** for do tipo incorreto ou fora do intervalo, com retornará o erro COMAdmin \_ E \_ SAFERINVALID. Se uma ativação de qualquer classificação falhar devido a verificações de confiança do SRP, COM retornará o erro CO \_ E \_ ACTIVATIONFAILED.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> <dt>

[**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)
</dt> <dt>

[**SRPRunningObjectChecks**](srprunningobjectchecks.md)
</dt> </dl>

 

 




