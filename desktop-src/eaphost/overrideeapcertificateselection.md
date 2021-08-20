---
title: OverrideEAPCertificateSelection
description: A chave do Registro OverrideEAPCertificateSelection determina se o cliente substituirá o comportamento de seleção de certificado de cartão inteligente padrão e fornecerá ao usuário mais certificados para escolher.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93efec6968fb27b0d27d88c696101815f0b48c36c100f78092d5b559d4c0f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085910"
---
# <a name="overrideeapcertificateselection"></a>OverrideEAPCertificateSelection

A chave do Registro OverrideEAPCertificateSelection determina se o cliente substituirá o comportamento de seleção de certificado de cartão inteligente padrão e fornecerá ao usuário mais certificados para escolher.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a>Comentários

Este é um **valor \_ BINARY** REG.



| Valor | Descrição                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x000 | Não substitua o comportamento padrão.                                                                                                                                                                |
| 0x001 | Escolha o último certificado anexado no cartão inteligente.                                                                                                                                            |
| 0x010 | Mostra todos os certificados na interface do usuário de seleção de certificado do cartão inteligente.                                                                                                                          |
| 0x100 | Mostra todos os certificados na interface do usuário de seleção de certificado do Registro.                                                                                                                            |
| 0x101 | Mostra todos os certificados na interface do usuário de seleção de certificado do Registro e o último certificado anexado do cartão inteligente. Mostra o último certificado anexado do cartão inteligente conforme selecionado. |
| 0x110 | Mostra todos os certificados na interface do usuário de seleção de certificado do registro e do cartão inteligente.                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registro EAPHost Configurações](eaphost-registry-settings.md)
</dt> </dl>

 

 




