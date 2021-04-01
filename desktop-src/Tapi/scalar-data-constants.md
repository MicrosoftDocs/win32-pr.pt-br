---
description: Para constantes de dados escalares extensíveis, um fornecedor de provedor de serviços pode definir novos valores em um intervalo especificado.
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: Constantes de dados escalares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3187d2064501727614dfcbf0b8e11c136fea13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663588"
---
# <a name="scalar-data-constants"></a>Constantes de dados escalares

Para constantes de dados escalares extensíveis, um fornecedor de provedor de serviços pode definir novos valores em um intervalo especificado. Como a maioria das constantes de dados são **DWORD** s, o intervalo 0x00000000 a 0x7FFFFFFF normalmente é reservado para extensões futuras comuns, enquanto 0X80000000 a 0xFFFFFFFF está disponível para extensões específicas do fornecedor. A suposição é que um fornecedor definiria valores que são extensões naturais dos tipos de texto definidos pela API.

 

 



