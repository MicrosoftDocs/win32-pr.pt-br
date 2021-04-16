---
description: 'Antes de colocar dados no registro, um aplicativo deve dividir os dados em duas categorias: dados específicos do computador e dados específicos do usuário.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Categorias de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753696"
---
# <a name="categories-of-data"></a>Categorias de dados

Antes de colocar dados no registro, um aplicativo deve dividir os dados em duas categorias: dados específicos do computador e dados específicos do usuário. Fazendo essa distinção, um aplicativo pode dar suporte a vários usuários e, ainda assim, localizar dados específicos do usuário em uma rede e usá-los em locais diferentes, permitindo dados de perfil de usuário independentes de local. (Um perfil de usuário é um conjunto de dados de configuração salvos para cada usuário.)

Quando o aplicativo é instalado, ele deve registrar os dados específicos do computador na chave **do \_ \_ computador local hKey** . Em particular, ele deve criar chaves para o nome da empresa, o nome do produto e o número de versão, conforme mostrado no exemplo a seguir:

**HKEY \_ O \_ \\ software \\ da máquina local**_MyCompany \\ MyProduct \\ 1,0_

Se o aplicativo oferecer suporte a COM, ele deverá registrar esses dados em **HKEY \_ local \_ Machine \\ software \\ classes**.

Um aplicativo deve registrar dados específicos do usuário sob a chave de **\_ \_ usuário atual hKey** , conforme mostrado no exemplo a seguir:

**HKEY \_ \_ \\ Software \\ do usuário atual**_MyCompany \\ MyProduct \\ 1,0_

 

 



