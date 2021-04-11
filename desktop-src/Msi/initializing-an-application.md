---
description: Para habilitar a funcionalidade do instalador, um aplicativo deve chamar várias funções quando ele estiver sendo inicializado.
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: Inicializando um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169185"
---
# <a name="initializing-an-application"></a>Inicializando um aplicativo

Para habilitar a funcionalidade do instalador, um aplicativo deve chamar várias funções quando ele estiver sendo inicializado. Para obter mais informações, consulte [mecanismo de instalação](installation-mechanism.md). As etapas a seguir descrevem como usar o instalador para inicializar um aplicativo:

**Para inicializar um aplicativo**

1.  Chame a função [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) para que o aplicativo possa se identificar para o instalador.

    O código do produto é um parâmetro necessário para muitas funções do instalador.

2.  Chame a função [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) para coletar informações do usuário na primeira vez que o aplicativo for iniciado.

    Se a chamada para [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) falhar, chame a função [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) para coletar informações do usuário.

3.  Exiba uma interface do usuário padrão, se necessário, chamando a função [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .

    Para criar sua própria interface de usuário, registre-a com o instalador chamando a função [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .

4.  Chame a função [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) para definir o nível de log.
5.  Apresente ao usuário os recursos disponíveis enumerando os recursos do seu aplicativo. Você pode enumerar recursos das seguintes maneiras:
    -   Consulte o recurso do instalador por recurso. Por exemplo, antes que o aplicativo desenhe um botão ou um item de menu, o aplicativo chama a função [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) para que o instalador possa verificar se o recurso está disponível.
    -   Enumere todos os recursos disponíveis de uma vez chamando a função [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) . Para usar essa função, o aplicativo deve chamar **MsiEnumFeatures** repetidamente enquanto incrementa um índice.
6.  Obtenha informações detalhadas sobre a instalação atual chamando as seguintes funções de enumeração repetidamente, incrementando uma variável de índice para cada chamada:

    -   Chame a função [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) para enumerar os produtos registrados com o instalador.
    -   Chame a função [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) para enumerar componentes.
    -   Chame a função [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) para enumerar qualificadores de componentes.
    -   Chame a função [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) para enumerar os produtos para um componente específico.

    Se o valor de retorno em uma função de enumeração for um erro de \_ êxito, ainda haverá mais itens a serem enumerados e a função deverá ser chamada novamente com uma variável de índice incrementada. Se o valor de retorno for \_ um erro de não \_ mais \_ itens, todos os itens foram enumerados e a função não deve ser chamada novamente.

 

 



