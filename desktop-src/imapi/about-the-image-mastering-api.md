---
title: Sobre a API de mestre de imagem
description: Esta documentação se concentra em uma descrição da implementação da Adaptec do IMAPi para Microsoft (IMAPIv1).
ms.assetid: 596ec3ea-17d1-4e60-8789-528ff00ae421
keywords:
- API de mestre de imagem IMAPi, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb16ab8c542e7c4686c7a3f4d027169a520495a8d3fab9927f11ed974deeef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451896"
---
# <a name="about-the-image-mastering-api"></a>Sobre a API de mestre de imagem

Esta documentação se concentra em uma descrição da implementação da Adaptec do IMAPi para Microsoft (IMAPIv1). Assim, as descrições dos quatro objetos COM principais e suas interfaces estão incluídas neste documento. Os quatro objetos principais são os seguintes: **MSDiscMasterObj**, **MSDiscRecorderObj**, **MSDiscStashObj** e **MSBurnEngineObj**.

Pode haver vários objetos **MSDiscMasterObj** instanciados em um sistema, mas apenas um aplicativo pode acessar um gravador por vez. O **MSDiscMasterObj** implementa várias interfaces, conforme mostrado no diagrama de objeto a seguir.

![o msdiscmasterobj implementa várias interfaces](images/imapi.png)

Os aplicativos usam a interface [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) para executar as seguintes tarefas:

-   Abrir IMAPi
-   Enumerar formatos com suporte (Joliet e Redbook)
-   Selecionar um formato
-   Obter uma lista de gravadores
-   Selecionar um gravador
-   Iniciar uma gravação

As interfaces [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) e [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) são retornadas a um aplicativo por meio da interface [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) quando um formato é selecionado. Essas interfaces controlam o conteúdo de um disco de dados ou áudio, respectivamente. Não se espera que todos os aplicativos compreendam as interfaces de formato específicas. Os aplicativos podem acessar as propriedades genéricas da interface **IJolietDiscMaster** , como o nome do volume ou o nome do arquivo herdado.

Os objetos **MSDiscRecorderObj** são acessados por meio da interface [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) . Cada dispositivo CD-R ou CD-RW compatível com o IMAPi tem um objeto **MSDiscRecorderObj** correspondente. Um aplicativo usa ponteiros para a interface **IDiscRecorder** nesses objetos para selecionar qual dispositivo será usado pelo IMAPI para gravar um CD. Além disso, os aplicativos podem acessar propriedades genéricas de um gravador por meio do **IDiscRecorder**. Isso inclui propriedades como velocidade do gravador ou outros parâmetros de gravação.

Os objetos restantes, **MSDiscStashObj** e **MSBurnEngineObj**, são objetos internos ACessados pelo IMAPI. Eles são mencionados aqui apenas para esclarecer a arquitetura do IMAPi. O **MSDiscStashObj** representa (por meio da interface **IDiscStash** ) um arquivo bruto de até 800 MB de tamanho que é usado pelo **MSDiscMasterObj** para criar imagens de áudio ou discos de dados a serem gravados. O stash é passado para o **MSBurnEngineObj** (por meio da interface **IMSBurnEngine** ) quando uma gravação é solicitada do mecanismo de nível inferior. O objeto **MSBurnEngineObj** espera que o conteúdo do Stash esteja em um formato conhecido. Nesse sentido, **MSDiscMasterObj** e **MSBurnEngineObj** têm um contrato com relação ao conteúdo do Stash.

 

 




