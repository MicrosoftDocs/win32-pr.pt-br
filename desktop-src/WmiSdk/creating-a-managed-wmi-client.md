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
ms.openlocfilehash: 6f28b01cb3b4506e0b47332cc3336af95dd641e78c7716f33b8e62b162081bdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071516"
---
# <a name="creating-a-managed-wmi-client"></a>Criando um cliente WMI gerenciado

A versão atual do WMI contém o namespace System. Management, que expõe uma série de APIs que interagem com o WMI. No entanto, não é recomendável que você use esse namespace.

se você quiser criar um cliente WMI gerenciado, é recomendável usar a infraestrutura de gerenciamento de Windows (MI). MI é a versão de última geração do WMI e contém suporte completo para código gerenciado. Para obter mais informações, consulte [como implementar um cliente mi gerenciado](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).

 

 
