---
description: o túnel automático com endereços compatíveis com IPv4 e 6to4 ambos funcionam por meio de uma rota para um prefixo que está no link para a interface \# 2. Os bits 32 após o prefixo são extraídos e usados como um endereço de destino IPv4 para o pacote encapsulado.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: 6to4 e túnel automático IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4170d937e331d38337c21b777ae232a39fcb304f8550a1d1ed994ef55101bb0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758486"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a>6to4 e túnel automático IPv6

o túnel automático com endereços compatíveis com IPv4 e 6to4 ambos funcionam por meio de uma rota para um prefixo que está no link para a interface \# 2. Os bits 32 após o prefixo são extraídos e usados como um endereço de destino IPv4 para o pacote encapsulado.

O túnel automático usa o prefixo::/96, que é habilitado por padrão. Ele pode ser desabilitado removendo a rota para::/96.

6to4 usa o prefixo 2002::/16, que não está habilitado por padrão.

 

 



