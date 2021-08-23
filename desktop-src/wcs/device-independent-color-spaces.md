---
title: Espaços de cores independentes do dispositivo
description: Reconhecendo a necessidade de medidas de cores padrão, independentes de dispositivo, a Comissão International de l'Eclairage (Comissão Internacional na iluminação) ou CIE, criou um espaço de cores baseado em \ 0034; imaginário \ 0034; cores primárias.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Windows Sistema de cores (WCS), espaços de cores independentes de dispositivo
- WCS (Windows sistema de cores), espaços de cores independentes de dispositivo
- gerenciamento de cores de imagem, espaços de cores independentes de dispositivo
- gerenciamento de cores, espaços de cores independentes de dispositivo
- cores, espaços de cores independentes de dispositivo
- espaços de cores, independentes de dispositivo
- espaços de cores independentes de dispositivo
- Commission International de l'Eclairage (CIE)
- CIE (Comissão Internacional de iluminação)
- CIE (Commission International de l'Eclairage)
- CIE (Comissão Internacional sobre iluminação)
- Espaço de cores CIEXYZ
- Espaço de cores XYZ
- espaço de cores sRGB
- espaços de cores, CIEXYZ
- espaços de cores, sRGB
- espaços de cores, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8c350ca4aa4b046d35926cd7568c4fbdfe030b7d7c13b085b9f3837c5dd8418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028784"
---
# <a name="device-independent-color-spaces"></a>Espaços de cores independentes do dispositivo

Reconhecendo a necessidade de medidas de cores padrão, independentes de dispositivo, a Comissão International de l'Eclairage (Comissão Internacional na iluminação) ou CIE, criou um [espaço de cores](c.md) com base em [cores primárias](p.md)"imaginários". Nenhum dispositivo real é esperado para produzir cores nesse espaço de cores. Ele é usado como um meio de converter cores de um espaço de cor para outro. As cores primárias nesse espaço de cores são as cores abstratas X, Y e Z.

O espaço de cores de 1931 CIEXYZ é amplamente usado como a base para conversão de espaço de cor. No entanto, com o crescimento da Internet, as considerações sobre largura de banda tornaram o espaço de cores XYZ incômodo. A troca de imagens sobre a largura de banda limitada da Internet exige um modelo de [cores](c.md)mais compacto.

Como resultado, a Hewlett-Packard e a Microsoft propuseram a adoção de um espaço de cores RGB predefinido padrão conhecido como sRGB, para permitir o gerenciamento preciso de cores com muito pouca sobrecarga de dados. Esse padrão foi aprovado como um padrão internacional formal pelo International Electrotechnical Commission (IEC) como IEC 61966-2-1: sistemas de multimídia e medição de EquipmentColour e ManagementPart 2-1: cor ManagementDefault o espaço de cores RGB. Ele está disponível diretamente do IEC em <https://www.iec.ch/> . As informações que abordam os problemas técnicos envolvidos no sRGB estão disponíveis na Internet em:

[Um espaço de cores padrão para a Internet-sRGB](https://www.w3.org/Graphics/Color/sRGB.html)

Uma versão de arquivo de ajuda de um white paper discutindo os problemas técnicos envolvidos em sRGB, sRGB. HLP, está disponível na \\ pasta de ajuda da referência do programador do WCS 1,0 no SDK da plataforma.

Formatos de arquivo diferentes podem usar ou adicionar um sinalizador para especificar que a imagem está no espaço de cores sRGB. no formato DIB (bitmap independente de dispositivo) Windows, definir o membro **bV5CSType** da estrutura [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) para LCS \_ sRGB especifica que as cores de DIB estão no espaço de cores sRGB.

 

 




