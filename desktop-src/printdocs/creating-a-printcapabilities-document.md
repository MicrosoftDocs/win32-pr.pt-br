---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Criando um documento de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccb1adf4626254ba9f71c706ad7d4556a23aeb6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105807857"
---
# <a name="creating-a-printcapabilities-document"></a>Criando um documento de PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Depois que um PrintTicket é validado, ele pode ser usado para criar um instantâneo dos PrintCapabilities. O provedor deve ter uma representação interna para qualquer propriedade cujo valor seja dependente da configuração do dispositivo. Por exemplo, se SpotDiameter for uma propriedade que depende dos recursos de resolução e de MediaType, uma representação interna de SpotDiameter, pois ele se relaciona com os vários valores para resolução e MediaType pode aparecer como na tabela a seguir:



| Resolução      | MediaType         | SpotDiameter   |
|-----------------|-------------------|----------------|
| 300<br/>  | Vincular<br/>   | 520<br/> |
| 300<br/>  | Acetinado<br/> | 350<br/> |
| 600<br/>  | Vincular<br/>   | 330<br/> |
| 600<br/>  | Acetinado<br/> | 180<br/> |
| 1200<br/> | Vincular<br/>   | 250<br/> |
| 1200<br/> | Acetinado<br/> | 100<br/> |



 

Para este exemplo, o provedor de PrintCapabilities deve usar o PrintTicket fornecido para selecionar a entrada apropriada da tabela interna e relatar que como o valor para a propriedade SpotDiameter. Esse processo é repetido para cada propriedade de valores múltiplos (para cada propriedade cujo valor é dependente da configuração). A seção [esquema de PrintCapabilities e construção de documentos](printcapabilities-schema-and-document-construction.md) descreve as outras etapas envolvidas na criação de um instantâneo dos PrintCapabilities.

Para criar um instantâneo do documento padrão de PrintCapabilities, forneça um PrintTicket padrão (em vez de um PrintTicket arbitrário) para o método que cria documentos de PrintCapabilities.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




