---
description: Para constantes de dados de sinalizador de bit extensível, um fornecedor de provedor de serviço pode definir novos valores para bits especificados.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Bit-Flag constantes de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789465"
---
# <a name="bit-flag-data-constants"></a>Bit-Flag constantes de dados

Para constantes de dados de sinalizador de bit extensível, um fornecedor de provedor de serviço pode definir novos valores para bits especificados. Como a maioria das constantes de sinalizador de bits é **DWORD** s, um número específico de bits inferiores geralmente é reservado para extensões comuns, enquanto os bits superiores restantes estão disponíveis para extensões específicas do fornecedor. Os sinalizadores de bits comuns são atribuídos do bit zero para cima e as extensões específicas do fornecedor devem ser atribuídas do bit 31 para baixo. Esse esquema fornece flexibilidade máxima na atribuição de posições de bits a extensões comuns, em oposição às extensões específicas do fornecedor. Um fornecedor deve definir novos valores que são extensões naturais dos sinalizadores de bits definidos pela API.

Estruturas de dados extensíveis têm um campo de tamanho de variavelmente reservado para uso específico do dispositivo. Como o campo é dimensionado de forma variada, o provedor de serviços decide a quantidade de informações e interpretação do campo. Um fornecedor que define um campo específico do dispositivo deve fazer essas extensões naturais da estrutura de dados original definida pela API.

 

 



