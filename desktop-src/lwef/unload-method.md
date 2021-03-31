---
title: Método Unload
description: Método Unload
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640753"
---
# <a name="unload-method"></a>Método Unload

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Descarrega os dados de caractere para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres. Unload "*** characterid * * *"**

</dd> </dl>

## <a name="remarks"></a>Comentários

Use esse método quando não precisar mais de um caractere, para liberar memória usada para armazenar informações sobre o caractere. Se você acessar o caractere novamente, use o método [**Load**](load-method.md) .

Esse método não retorna um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .

 

 