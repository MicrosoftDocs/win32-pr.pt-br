---
description: Esta seção descreve as estruturas do reconhecedor.
ms.assetid: 4c17391f-7af4-42ab-b77f-e3c39cadc0b6
title: Estruturas do reconhecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addaccf3e69f35b99379710d681fe8ac45559ea1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797991"
---
# <a name="recognizer-structures"></a>Estruturas do reconhecedor

Esta seção descreve as estruturas do reconhecedor.

## <a name="in-this-section"></a>Nesta seção



| Estrutura                                                    | Descrição                                                                                                                                                   |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**intervalo de caracteres \_**](/windows/win32/api/rectypes/ns-rectypes-character_range)                  | Especifica um intervalo de pontos Unicode (caracteres).<br/>                                                                                                  |
| [**\_métricas de malha**](/windows/win32/api/rectypes/ns-rectypes-lattice_metrics)                  | Descreve a linha de base e a altura Tabs no meio.<br/>                                                                                                     |
| [**segmento de linha \_**](/windows/win32/api/rectypes/ns-rectypes-line_segment)                        | Descreve os pontos inicial e final de um segmento de reconhecimento de linha, como a linha de base ou Tabs no meio.<br/>                                                 |
| [**Descrição do pacote \_**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)            | Descreve o conteúdo do pacote para um contexto de Tablet específico.<br/>                                                                               |
| [**Propriedade de pacote \_**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)                  | Descreve uma propriedade de pacote que é relatada pelo driver do Tablet.<br/>                                                                                 |
| [**\_métricas de propriedade**](/windows/desktop/api/tpcshrd/ns-tpcshrd-property_metrics)                | Define o intervalo e a resolução de uma propriedade de pacote.<br/>                                                                                             |
| [**RECUP \_ ATTRS**](/windows/win32/api/rectypes/ns-rectypes-reco_attrs)                            | Recupera os atributos de um reconhecedor ou especifica quais atributos usar ao pesquisar por um reconhecedor instalado.<br/>                         |
| [**Guia do RECUP \_**](/windows/win32/api/rectypes/ns-rectypes-reco_guide)                            | Define os limites da tinta para o reconhecedor.<br/>                                                                                               |
| [**RECUP \_ malha**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)                        | Serve como o ponto de entrada para um malha.<br/>                                                                                                          |
| [**\_coluna recup malha \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)         | Representa uma coluna no malha.<br/>                                                                                                                |
| [**\_elemento recup malha \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)       | Corresponde a uma palavra ou um caractere do leste asiático, normalmente; no entanto, um elemento também pode corresponder a um gesto, uma forma ou algum outro código.<br/> |
| [**Propriedades de RECUP \_ malha \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties) | Contém uma matriz de ponteiros para estruturas de propriedade.<br/>                                                                                              |
| [**\_Propriedade recup malha \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)     | Contém uma propriedade usada no malha.<br/>                                                                                                           |
| [**intervalo de RECUP \_**](/windows/win32/api/rectypes/ns-rectypes-reco_range)                            | Identifica um intervalo de caracteres na cadeia de caracteres de resultado.<br/>                                                                                             |
| [**intervalo de traços \_**](/windows/win32/api/tpcshrd/ns-tpcshrd-stroke_range)                        | Especifica um intervalo de traços no objeto [**InkDisp**](inkdisp-class.md) .<br/>                                                                       |



 

 

 




