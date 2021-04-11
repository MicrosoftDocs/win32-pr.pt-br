---
title: Como a ADSI integra extensões
description: Diretrizes que descrevem como o ADSI interage com extensões.
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- ADSI de extensões
- ADSI e extensões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008361"
---
# <a name="how-adsi-integrates-extensions"></a>Como a ADSI integra extensões

As diretrizes a seguir descrevem como o ADSI interage com extensões:

-   Algo é associado a um objeto de diretório ADSI. Por exemplo, "LDAP:Binding = JeffSmith, OU = Sales, DC = Fabrikam, DC = COM".
-   A ADSI identifica que o objeto está na classe de **usuário** .
-   O ADSI executa uma pesquisa no registro e identifica os CLSIDs de extensão para o **usuário**. Lembre-se de que o ADSI armazena esses dados em cache.
-   Algo chama o método **QueryInterface** para IID \_ IMyExtension. A ADSI pesquisa as interfaces associadas ao objeto de **usuário** , começando com suas próprias interfaces e, em seguida, examinando as interfaces de extensão.
-   Se uma correspondência for encontrada, a ADSI criará uma instância do componente que dá suporte a IMyExtension de IID \_ e chamará **QueryInterface** para a extensão. A interface resultante é retornada.
-   O usuário usa essa interface para chamar os métodos de interface.
-   Em seguida, o cliente chama **QueryInterface** para IID \_ IYourExtension, que está em um componente diferente. Esse componente Delega essa chamada de **QueryInterface** para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do agregador, que é a própria ADSI.
-   Novamente, a ADSI pesquisa as interfaces e cria a instância do componente.

 

 