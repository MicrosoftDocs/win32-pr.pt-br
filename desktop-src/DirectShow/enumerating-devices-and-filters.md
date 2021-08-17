---
description: Enumerando dispositivos e filtros
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Enumerando dispositivos e filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53f4a36e2bf994cfeab34a49444d104b2213a839bb1fa8bd2aa4d70e0003b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401770"
---
# <a name="enumerating-devices-and-filters"></a>Enumerando dispositivos e filtros

Às vezes, um aplicativo precisa localizar um filtro específico no sistema do usuário. Por exemplo, um aplicativo de captura de vídeo pode exibir uma lista de dispositivos de captura disponíveis. como DirectShow usa uma arquitetura baseada em componentes, você não pode saber em tempo de design quais filtros estão instalados no sistema do usuário. Isso é particularmente verdadeiro para filtros que representam dispositivos de hardware. DirectShow fornece dois componentes que localizam filtros registrados:

-   O [enumerador de dispositivo do sistema](system-device-enumerator.md) localiza filtros por sua categoria.
-   O [mapeador de filtro](filter-mapper.md) localiza filtros de acordo com os critérios de pesquisa fornecidos pelo aplicativo.

Os enumeradores abordados nesta seção seguem o formulário padrão usado pelas interfaces de enumeração COM. Para obter mais informações, consulte o tópico "IEnumXXXX" no SDK (Software Development Kit) do Microsoft Platform.

Esta seção contém os seguintes tópicos:

-   [Usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md)
-   [Usando o mapeador de filtro](using-the-filter-mapper.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[tarefas básicas de DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 



