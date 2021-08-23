---
description: O tipo de dados GUID é uma cadeia de caracteres de texto que representa um ID (identificador de classe). COM deve ser capaz de converter a cadeia de caracteres em uma ID de Classe válida. Todos os GUIDs devem ser autores em letras maiúsculas.
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: GUID (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e92688e11d71a51c59a2edc6c3e50ed01ab246c83bf4cfb9ac67b8d6318766b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649336"
---
# <a name="guid"></a>GUID

O tipo de dados GUID é uma cadeia de caracteres de texto que representa um ID (identificador de classe). COM deve ser capaz de converter a cadeia de caracteres em uma ID de Classe válida. Todos os GUIDs devem ser autores em letras maiúsculas.

O formato válido para um GUID é {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} em que X é um dígito hexab (0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F).

Observe que utilitários como GUIDGEN podem gerar GUIDs contendo letras minúsculas. Todos eles devem ser alterados para letras maiúsculas antes que o GUID possa ser usado pelo instalador como um código de produto válido, código do pacote ou código do componente.

 

 



