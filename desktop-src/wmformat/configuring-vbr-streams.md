---
title: Configurando fluxos de VBR
description: Configurando fluxos de VBR
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- fluxos, configurando fluxos de VBR
- fluxos, taxa de bits variável (VBR)
- taxa de bits variável (VBR), fluxos
- VBR (taxa de bits variável), fluxos
- fluxos, interface IWMPropertyVault
- IWMPropertyVault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916984"
---
# <a name="configuring-vbr-streams"></a>Configurando fluxos de VBR

Você pode usar a codificação de taxa de bits variável (VBR) para produzir fluxos de alta qualidade para arquivos locais ou para download e reprodução. Há três opções de VBR: baseada em qualidade (uma passagem), não restrita (duas passagens) e restrita (duas passagens)... Para obter mais informações sobre os tipos de codificação de VBR, consulte [codificação de taxa de bits variável (VBR)](variable-bit-rate--vbr--encoding.md).

Você pode configurar a codificação de VBR em um perfil definindo propriedades com a interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) . A tabela a seguir descreve as propriedades usadas para configurar a codificação de VBR.



| Propriedade                     | Descrição                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| **g \_ wszVBREnabled**         | $True. Defina como true para usar a codificação de VBR.                                                   |
| **g \_ wszVBRQuality**         | Valor **DWORD** . Defina para o nível de qualidade desejado (de 1 a 100) para a codificação de VBR com base na qualidade.      |
| **g \_ wszVBRBitrateMax**      | Valor **DWORD** . Defina como a taxa de bits máxima, em bits por segundo, para a codificação de VBR restrita.   |
| **g \_ wszVBRBufferWindowMax** | Valor **DWORD** . Defina para a janela de buffer máximo, em milissegundos, para a codificação de VBR restrita. |



 

As seções a seguir descrevem como usar os diferentes tipos de codificação de taxa de bits variável.



| Seção                                                              | Descrição                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Para configurar Quality-Based VBR](to-configure-quality-based-vbr.md) | Descreve como usar a codificação de taxa de bits variável com base em um nível de qualidade estática.                                   |
| [Para configurar a VBR não restringida](to-configure-unconstrained-vbr.md) | Descreve como usar a codificação de taxa de bits variável com base em uma taxa de bits média de destino sem um valor de pico explícito. |
| [Para configurar a VBR restrita](to-configure-constrained-vbr.md)     | Descreve como usar a codificação de taxa de bits variável com base em uma taxa de bits média de destino e um valor de pico explícito.     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando fluxos**](configuring-streams.md)
</dt> </dl>

 

 




