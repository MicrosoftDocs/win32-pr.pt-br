---
description: O Windows instalador usa o idioma do usuário atual em todos os diálogos até que um pacote Windows instalador seja aberto.
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: Localizando o idioma exibido por diálogos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72142ce0f479379ebc929807294e6bbab7699738ee41e70be87e8e65f57c1ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043176"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a>Localizando o idioma exibido por diálogos

O Windows instalador usa o idioma do usuário atual em todos os diálogos até que um pacote Windows instalador seja aberto. O Windows instalador de dados determina isso usando **GetUserDefaultUILanguage**. Quando um Windows instalador é aberto, o instalador exibe diálogos usando o idioma do pacote, conforme especificado pela propriedade [**Resumo do**](template-summary.md) Modelo.

Para obter mais informações sobre como localizador o idioma de um pacote Windows Instalador, consulte também [Um exemplo de localização](a-localization-example.md).

 

 



