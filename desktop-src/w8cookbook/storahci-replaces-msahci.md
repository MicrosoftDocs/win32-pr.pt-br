---
title: StorAHCI substitui MSAHCI
description: StorAHCI substitui MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105761514"
---
# <a name="storahci-replaces-msahci"></a>StorAHCI substitui MSAHCI

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

O StorAHCI, uma miniporta Storport, dá suporte aos controladores AHCI (Serial Advanced Technology Attachment) avançados do controlador de host no Windows e substitui o MSAHCI, uma miniporta ATAport.

## <a name="manifestation"></a>Manifestação

Não deve haver nenhuma alteração na funcionalidade ou no desempenho; Esse driver dá suporte a todos os mesmos dispositivos aos quais o MSAHCI dá suporte.

Essa alteração é transparente para o usuário.

## <a name="mitigation"></a>Atenuação

Atualize todos os utilitários e scripts que dependem de associações ATAport. Não confie no nome da unidade. Em vez disso, use a detecção de disco padrão.

 

 




