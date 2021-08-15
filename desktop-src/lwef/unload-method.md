---
title: Método Unload
description: Método Unload
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74f274f758e34416cc73d82963fa21fbd93b14e7b6492c693f24b763081b49f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474494"
---
# <a name="unload-method"></a>Método Unload

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Descarrega os dados de caractere para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente ***. Caracteres. Unload "**_characterid_*_"_*

</dd> </dl>

## <a name="remarks"></a>Comentários

Use esse método quando não precisar mais de um caractere, para liberar memória usada para armazenar informações sobre o caractere. Se você acessar o caractere novamente, use o método [**Load**](load-method.md) .

Esse método não retorna um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .

 

 