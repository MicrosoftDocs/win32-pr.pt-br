---
description: Transformações de Media Foundation
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Transformações de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0518ced06169f6d998bdad1747878d109e0676
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105764550"
---
# <a name="media-foundation-transforms"></a>Transformações de Media Foundation

Transformações de Media Foundation (MFTs) fornecem um modelo genérico para o processamento de dados de mídia. MFTs são usados para decodificadores, codificadores e processadores de sinais digitais (DSPs). Em suma, tudo que fica no pipeline de mídia entre a origem da mídia e o coletor de mídia é uma MFT.

Esta seção descreve o modelo de programação MFT e como implementar um MFT, com recomendações para tipos específicos de MFTs, como decodificadores.



| Tópico                                                                    | Descrição                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre o MFTs](about-mfts.md)                                             | Fornece uma breve visão geral do MFTs                                                                                                                                                                   |
| [Modelo de processamento de MFT básico](basic-mft-processing-model.md)             | Descreve em mais detalhes o modelo básico para processamento de dados com um MFT.                                                                                                                           |
| [MFTs assíncrona](asynchronous-mfts.md)                               | Descreve um modelo de processamento assíncrono que é uma alternativa ao modelo básico.<br/> O processamento assíncrono foi introduzido no Windows 7. Nem todo MFT dá suporte a esse modelo.<br/> |
| [Registrando e enumerando MFTs](registering-and-enumerating-mfts.md) | Como registrar um MFT e como enumerar MFTs no registro.                                                                                                                                   |
| [Campo de restrições de uso](field-of-use-restrictions.md)               | Descreve o mecanismo para desbloquear um MFT que tem restrições de campo de uso.                                                                                                                    |
| [Comparação de MFTs e DMOs](comparison-of-mfts-and-dmos.md)           | Resume as diferenças entre MFTs e DMOs.                                                                                                                                                   |
| [Gravando uma MFT personalizada](writing-a-custom-mft.md)                         | Diretrizes para gravar um MFT personalizado.                                                                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de Media Foundation](media-foundation-pipeline.md)
</dt> <dt>

[Arquitetura Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




