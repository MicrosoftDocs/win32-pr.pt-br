---
description: Ao corrigir arquivos com conteúdo de variável, pode ser necessário reter as regiões selecionadas do arquivo de destino para evitar a perda de informações críticas.
ms.assetid: 4a610588-556e-489f-ac14-73e5e6b776fe
title: Aplicação de patch nas regiões selecionadas de um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778df4b0cc98eeacd1106929b18c7461c6fa9e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747957"
---
# <a name="patching-selected-regions-of-a-file"></a>Aplicação de patch nas regiões selecionadas de um arquivo

Ao corrigir arquivos com conteúdo de variável, pode ser necessário reter as regiões selecionadas do arquivo de destino para evitar a perda de informações críticas. Por exemplo, alguns aplicativos carimbam as informações do usuário no arquivo executável. Como o conteúdo do arquivo de destino pode depender do computador no qual o aplicativo está instalado, fica difícil determinar se um arquivo específico é um destino válido para o patch. As informações do usuário gravadas no arquivo de destino também podem ser substituídas por um patch.

Ao gerar um arquivo PCP (Propriedades de criação de patch) com [Msimsp.exe](msimsp-exe.md) e [PATCHWIZ.DLL](patchwiz-dll.md), você pode especificar que as informações em determinadas regiões do arquivo de destino sejam ignoradas durante a aplicação de patch. Você também pode especificar que as informações em outras regiões do arquivo de destino sejam retidas e copiadas para um local de deslocamento no arquivo atualizado. Especifique quais regiões do arquivo de destino ignorar e quais regiões manter ao criar as tabelas [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md), [ExternalFiles](externalfiles-table-patchwiz-dll-.md)e [FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md) .

Use a coluna RetainOffsets da tabela [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) e as colunas RetainOffsets e RetainLengths da tabela [FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md) para copiar um intervalo de informações do arquivo de destino para um intervalo de deslocamento no arquivo atualizado. As informações neste intervalo são mantidas. Especifique o comprimento do intervalo usando as colunas RetainLengths da tabela FamilyFileRanges. O comprimento do intervalo retido é o mesmo nos arquivos de destino e atualizados. Especifique o deslocamento do intervalo no arquivo de destino usando a coluna RetainOffsets da tabela TargetFiles OptionalData. Especifique o deslocamento do intervalo no arquivo atualizado usando a coluna RetainOffsets da tabela FamilyFileRanges. O intervalo do arquivo de destino retido é, portanto, o valor de RetainOffsets na tabela TargetFiles OptionalData mais RetainLengths. Essas informações são copiadas para o arquivo de atualização no intervalo fornecido pelo valor de RetainOffsets nas tabelas FamilyFileRanges mais RetainLengths. Você pode especificar vários intervalos, mas a ordem dos comprimentos deve corresponder à ordem dos deslocamentos.

Use a tabela [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) para ignorar um intervalo do arquivo de destino. As informações nesse intervalo do arquivo de destino ainda podem ser substituídas pelo patch. Especifique o deslocamento do intervalo na coluna IgnoreOffsets e seu comprimento na coluna IgnoreLengths. Você pode especificar vários intervalos, mas a ordem dos comprimentos deve corresponder à ordem dos deslocamentos.

Os valores nas colunas comprimentos e deslocamentos podem ser decimal ou hexadecimal. [PATCHWIZ.DLL](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x". As colunas são colunas de cadeia de caracteres, portanto PATCHWIZ.DLL converte os valores em ULONGs. A coluna Length especifica o comprimento em bytes.

 

 



