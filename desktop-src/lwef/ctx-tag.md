---
title: Marca de CTX
description: Marca de CTX
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7071994e741cb7dfd1147f163f0d7ef6299ec0dcb9d568ad068251d5a9436809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726089"
---
# <a name="ctx-tag"></a>Marca de CTX

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Define o contexto do texto de saída.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

\\**CTX** = *cadeia de caracteres*\\



| Parte     | Descrição                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Uma cadeia de caracteres que especifica o contexto do texto a seguir, que determina como os símbolos ou as abreviações são falados.<br/> **"Endereço"**    Endereços e/ou números de telefone.<br/> **"Email"**    Email.<br/> O contexto **"desconhecido"** (padrão) é desconhecido.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Essa marca só tem suporte para a saída gerada por TTS. O intervalo de valores para o parâmetro pode variar dependendo do mecanismo de TTS instalado.

 

 





