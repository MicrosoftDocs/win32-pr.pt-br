---
description: Enumerando dispositivos e filtros
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Enumerando dispositivos e filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825922"
---
# <a name="enumerating-devices-and-filters"></a>Enumerando dispositivos e filtros

Às vezes, um aplicativo precisa localizar um filtro específico no sistema do usuário. Por exemplo, um aplicativo de captura de vídeo pode exibir uma lista de dispositivos de captura disponíveis. Como o DirectShow usa uma arquitetura baseada em componentes, você não pode saber em tempo de design quais filtros estão instalados no sistema do usuário. Isso é particularmente verdadeiro para filtros que representam dispositivos de hardware. O DirectShow fornece dois componentes que localizam filtros registrados:

-   O [enumerador de dispositivo do sistema](system-device-enumerator.md) localiza filtros por sua categoria.
-   O [mapeador de filtro](filter-mapper.md) localiza filtros de acordo com os critérios de pesquisa fornecidos pelo aplicativo.

Os enumeradores abordados nesta seção seguem o formulário padrão usado pelas interfaces de enumeração COM. Para obter mais informações, consulte o tópico "IEnumXXXX" no SDK (Software Development Kit) do Microsoft Platform.

Esta seção contém os seguintes tópicos:

-   [Usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md)
-   [Usando o mapeador de filtro](using-the-filter-mapper.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas básicas do DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 



