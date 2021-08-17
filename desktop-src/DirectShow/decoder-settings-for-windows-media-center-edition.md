---
description: Configurações do decodificador para Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Configurações do decodificador para Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc373f2ea58bc169748ff42841650cf979822014e579a78459e47da5c694814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953155"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a>Configurações do decodificador para Windows Media Center Edition

Windows O XP Media Center Edition 2005 e posterior usa a interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) para configurar o filtro de decodificador de áudio para reprodução de televisão e DVD. Há suporte para as seguintes propriedades.



| GUID da propriedade                   | Descrição                                      |
|---------------------------------|--------------------------------------------------|
| \_formato de \_ saída de áudio CODECAPI \_ | Configura o formato de saída de áudio. Consulte Observações. |



 

## <a name="remarks"></a>Comentários

O valor da propriedade de \_ formato de saída de áudio CODECAPI \_ \_ é uma representação de cadeia de caracteres de um GUID, armazenado como um valor **BSTR** . Os GUIDs a seguir são definidos.



| GUID                                                        | Descrição                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_formato de saída de áudio CODECAPI \_ \_ \_ \_ MATRIXENCODED estéreo PCM \_ | O filtro de áudio de software deve executar a decodificação de software e a saída de um fluxo de áudio estéreo, com a matriz de áudio multicanal codificada para os dois canais.                                                   |
| \_formato de saída de áudio CODECAPI \_ \_ \_ \_ estéreo PCM                | O filtro de áudio de software deve executar a decodificação de software e gerar um fluxo de áudio estéreo.                                                                                                                   |
| \_ \_ \_ PCM SPDIF de formato de saída \_ de áudio CODECAPI \_                 | O filtro de áudio de software deve executar a decodificação de áudio de software, mesmo que a saída física do PC possa ser uma interface digital, como S/PDIF.                                                      |
| \_formato de saída de áudio CODECAPI \_ \_ \_ SPDIF \_ fragmentado           | O filtro de áudio de software não deve executar a decodificação de áudio de software, mas deve passar o fragmentado de áudio digital bruto para processamento externo por um dispositivo conectado com um link de áudio digital, como S/PDIF. |
| \_fone de \_ \_ \_ ouvido PCM do formato de saída de áudio CODECAPI \_            | O filtro de áudio de software deve executar a decodificação de áudio de software e deve aplicar o processamento proprietário para otimizar para fones de ouvido. O suporte para essa configuração é opcional.                                     |



 

> [!Note]  
> A interface **ICodecAPI** armazena propriedades de codec como pares de chave/valor, onde a chave é um GUID e o valor é um tipo de **variante** .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificador e desenvolvimento de decodificador](encoder-and-decoder-development.md)
</dt> </dl>

 

 



