---
description: Saiba mais sobre como adicionar instâncias de propriedade. O esquema de impressão permite que as instâncias de propriedade estejam presentes em uma instância de opção.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Adicionando instâncias de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8085fa10f824f32dc76aef0f1e5f78ca05b22b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409689"
---
# <a name="adding-property-instances"></a>Adicionando instâncias de propriedade

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O esquema de impressão permite que as instâncias de propriedade estejam presentes em uma instância de opção. As instâncias de propriedade definidas no documento PrintCapabilities não são propagadas para as instâncias de opção salvas no PrintTicket. Os elementos de propriedade não afetam o resultado do processo de Pontuação quando duas instâncias de opção são comparadas, mas as instâncias ScoredProperty afetam esse processo. Todos os drivers de dispositivo que implementam um algoritmo de Pontuação devem observar essa convenção. Os provedores de PrintCapabilities têm permissão para adicionar instâncias de propriedade a uma opção se essas instâncias forem específicas para essa opção específica e nenhuma outra, ou se o provedor pretender que o valor dessa propriedade apareça para cada opção no recurso. Por exemplo, suponha que a propriedade de taxa de fotonotação seja dependente da opção selecionada para o recurso PageResolution. Se a propriedade de impressão for colocada no nível raiz do documento PrintCapabilities, ela seria de valor único e refletiria apenas a taxa de impressão para a resolução selecionada no momento. No entanto, se a propriedade de taxa de impressão tiver sido colocada dentro de cada opção PageResolution, cada instância da propriedade Print Rate poderá refletir a taxa impressa para a opção PageResolution que a continha. O documento PrintCapabilities contém várias definições para a taxa de fotonota, uma correspondente a cada opção PageResolution. Usando uma representação abreviada, as PrintCapabilities contêm:

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

Em algumas situações, colocar uma propriedade de taxa de impressão dentro de cada opção de resolução é mais conveniente para o cliente, pois o cliente pode determinar rapidamente o efeito que cada opção de resolução tem na taxa de impressão, sem a necessidade de obter um novo documento de PrintCapabilities para cada configuração de resolução.

Observe também que as instâncias de propriedade também podem ser adicionadas como elementos filho dos elementos de recurso. Isso será útil se houver instâncias de propriedade ou valores de instâncias de propriedade que são específicos de cada recurso. Por exemplo, pode haver uma propriedade que especifica se apenas uma opção pode ser selecionada ao mesmo tempo para um recurso ou se várias opções podem ser selecionadas. Esse é o escolha \_ um, escolha \_ muitas propriedades usadas nos arquivos PPD e GPD. Como algumas instâncias de recurso podem ser identificadas como escolha \_ uma, enquanto outras podem ser identificadas como escolher \_ muitos, essa propriedade deve ser definida para cada recurso. A localização da propriedade como um elemento filho do recurso produz a associação entre a propriedade e o recurso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



