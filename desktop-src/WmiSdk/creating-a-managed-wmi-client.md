---
description: Atualmente, o WMI não oferece suporte a código gerenciado no WMI, mas tem suporte em MI.
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: Criando um cliente WMI gerenciado
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb1339347c4e15cd29ebf4d4e98e5a8b61a24e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782418"
---
# <a name="creating-a-managed-wmi-client"></a>Criando um cliente WMI gerenciado

A versão atual do WMI contém o namespace System. Management, que expõe uma série de APIs que interagem com o WMI. No entanto, não é recomendável que você use esse namespace.

Se você quiser criar um cliente WMI gerenciado, é recomendável usar o MI (infraestrutura de gerenciamento do Windows). MI é a versão de última geração do WMI e contém suporte completo para código gerenciado. Para obter mais informações, consulte [como implementar um cliente mi gerenciado](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).

 

 
