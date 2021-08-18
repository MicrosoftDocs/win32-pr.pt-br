---
description: 'Antes de colocar dados no Registro, um aplicativo deve dividir os dados em duas categorias: dados específicos do computador e dados específicos do usuário.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Categorias de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad4bf4abb7af2abf723aa42f3426c58230083d8e575dda176b8eeda0daecb36d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885847"
---
# <a name="categories-of-data"></a>Categorias de dados

Antes de colocar dados no Registro, um aplicativo deve dividir os dados em duas categorias: dados específicos do computador e dados específicos do usuário. Ao fazer essa distinção, um aplicativo pode dar suporte a vários usuários e ainda localizar dados específicos do usuário em uma rede e usar esses dados em locais diferentes, permitindo dados de perfil de usuário independentes de localização. (Um perfil de usuário é um conjunto de dados de configuração salvos para cada usuário.)

Quando o aplicativo é instalado, ele deve registrar os dados específicos do computador na **chave HKEY \_ LOCAL \_ MACHINE.** Em particular, ele deve criar chaves para o nome da empresa, o nome do produto e o número de versão, conforme mostrado no exemplo a seguir:

**HKEY \_ SOFTWARE \_ LOCAL \\ \\ MACHINE**_MyCompany \\ MyProduct \\ 1.0_

Se o aplicativo for compatível com COM, ele deverá registrar esses dados em **Classes de Software HKEY \_ LOCAL \_ MACHINE \\ \\**.

Um aplicativo deve registrar dados específicos do usuário na **chave HKEY \_ CURRENT \_ USER,** conforme mostrado no exemplo a seguir:

**HKEY \_ CURRENT \_ USER \\ \\ Software**_MyCompany \\ MyProduct \\ 1.0_

 

 



