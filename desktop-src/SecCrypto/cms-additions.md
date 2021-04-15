---
description: A sintaxe de mensagem de criptografia (CMS), derivada da \# versão 1,5 do PKCS 7, é a sintaxe usada para fazer hash, assinar digitalmente, autenticar e criptografar mensagens arbitrárias.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: Adições de CMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753927"
---
# <a name="cms-additions"></a>Adições de CMS

A sintaxe de mensagem de criptografia (CMS), derivada da \# versão 1,5 do PKCS 7, é a sintaxe usada para fazer [*hash*](../secgloss/h-gly.md), [*assinar digitalmente*](../secgloss/d-gly.md), autenticar e criptografar mensagens arbitrárias. Sempre que possível, a compatibilidade com versões anteriores é preservada; no entanto, foram feitas alterações para acomodar a transferência de certificado de atributo e técnicas de contrato de chave para o gerenciamento de chaves. O CMS permite vários encapsulamentos para que um envelope de encapsulamento possa ser aninhado dentro de outro. Além disso, uma parte pode assinar digitalmente os dados encapsulados anteriormente; atributos arbitrários, como o tempo de assinatura, podem ser assinados junto com o conteúdo da mensagem; atributos e, como [*referendas*](../secgloss/c-gly.md), podem ser associados a uma assinatura. O CMS pode dar suporte a várias arquiteturas para o gerenciamento de chaves baseado em certificado.

Para dar suporte a recursos adicionais do CMS, as estruturas de dados subjacentes receberam novos campos. Novos sinalizadores e valores de parâmetros também foram adicionados. Todas as estruturas de dados e todas as APIs que usam o CMS são compatíveis com 100% de compatibilidade com PKCS \# 7 versão 1,5.

As adições incluem [adições de dados envelopadas](enveloped-data-additions.md) e [adições de dados assinadas](signed-data-additions.md).

 

 
