---
title: StorAHCI substitui MSAHCI
description: StorAHCI substitui MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6affffe41dd00c009ebb7bebf508dac1b63bec673c17783f594d22969822e542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932136"
---
# <a name="storahci-replaces-msahci"></a>StorAHCI substitui MSAHCI

## <a name="platforms"></a>Plataformas

**clientes** – Windows 8  
**servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

StorAHCI, uma miniporta Storport, dá suporte aos controladores AHCI (serial advanced technology attachment) avançados do controlador de host em Windows e substitui MSAHCI, uma miniporta ATAport.

## <a name="manifestation"></a>Manifestação

Não deve haver nenhuma alteração na funcionalidade ou no desempenho; Esse driver dá suporte a todos os mesmos dispositivos aos quais o MSAHCI dá suporte.

Essa alteração é transparente para o usuário.

## <a name="mitigation"></a>Atenuação

Atualize todos os utilitários e scripts que dependem de associações ATAport. Não confie no nome da unidade. Em vez disso, use a detecção de disco padrão.

 

 




