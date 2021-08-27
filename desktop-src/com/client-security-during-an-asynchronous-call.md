---
title: Client Security durante uma chamada assíncrona
description: Client Security durante uma chamada assíncrona
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4c25e17712d0164938f3de9895d1e6b02582f2d86cba9957297e23aa4e7f1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071036"
---
# <a name="client-security-during-an-asynchronous-call"></a>Client Security durante uma chamada assíncrona

O Gerenciador de proxy criado pelo MIDL para objetos que usam marshaling padrão implementa a interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) . Os clientes podem gerenciar a segurança de chamadas com marshaling consultando **IClientSecurity** no objeto de chamada e obtendo ou alterando as configurações de segurança.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fazendo uma chamada assíncrona](making-an-asynchronous-call.md)
</dt> </dl>

 

 




