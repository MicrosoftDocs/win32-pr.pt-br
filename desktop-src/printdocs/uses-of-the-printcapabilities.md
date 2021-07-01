---
description: Saiba mais sobre os usos de PrintCapabilities. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Usos de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09882d42814930ef5ba08e087f1df87e0d0e9bc
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119421"
---
# <a name="uses-of-the-printcapabilities"></a>Usos de PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

As PrintCapabilities destinam-se a representar atributos de dispositivo configuráveis como constructos de recurso/opção ou constructos de parâmetro. Essas informações definem o espaço de configuração do dispositivo e podem ser usadas por um cliente de interface do usuário para construir uma interface do usuário. As Palavras-chave de esquema de impressão definem um conjunto de instâncias de recurso padrão, instâncias option para as instâncias de Recurso padrão e instâncias ParameterDef.

Os constructos de recurso/opção ou parâmetro em PrintCapabilities destinam-se a manter instâncias property ou ScoredProperty que descrevem um dispositivo e que têm suporte pelo subsistema spooler. Essas instâncias Property e ScoredProperty são de interesse geral para os clientes do dispositivo e contêm as informações fornecidas pelas funções Win32 DevCaps. As Palavras-chave de esquema de impressão definem um conjunto de instâncias Padrão de Propriedade e ScoredProperty.

É necessário enfatizar que o documento PrintCapabilities destina-se a representar apenas dados com valor único: dados que não dependem de uma configuração específica do dispositivo. O documento PrintCapabilities fornece apenas um instantâneo de dados dependentes de configuração.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



