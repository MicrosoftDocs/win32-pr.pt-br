---
title: OverrideEAPCertificateSelection
description: A chave do registro OverrideEAPCertificateSelection determina se o cliente substituirá o comportamento de seleção de certificado de cartão inteligente padrão e fornecerá a ele mais certificados para sua escolha.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103823488"
---
# <a name="overrideeapcertificateselection"></a>OverrideEAPCertificateSelection

A chave do registro OverrideEAPCertificateSelection determina se o cliente substituirá o comportamento de seleção de certificado de cartão inteligente padrão e fornecerá a ele mais certificados para sua escolha.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ binário reg** .



| Valor | Descrição                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x000 | Não substitua o comportamento padrão.                                                                                                                                                                |
| 0x001 | Escolha o último certificado anexado do cartão inteligente.                                                                                                                                            |
| 0x010 | Mostra todos os certificados na interface do usuário de seleção de certificado do cartão inteligente.                                                                                                                          |
| 0x100 | Mostra todos os certificados na interface do usuário de seleção de certificado do registro.                                                                                                                            |
| 0x101 | Mostra todos os certificados na interface do usuário de seleção de certificado do registro e o último certificado anexado do cartão inteligente. Mostra o último certificado anexado do cartão inteligente, conforme selecionado. |
| 0x110 | Mostra todos os certificados na interface do usuário de seleção de certificado do registro e do cartão inteligente.                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurações do registro EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




