---
title: Marca de CTX
description: Marca de CTX
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005758"
---
# <a name="ctx-tag"></a>Marca de CTX

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

 

 





