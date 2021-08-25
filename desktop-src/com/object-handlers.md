---
title: Manipuladores de objetos
description: Manipuladores de objetos
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85221456d637e0d9e982aad253c06d34618018a3648a31a7bd21e8c1465fa84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992316"
---
# <a name="object-handlers"></a>Manipuladores de objetos

Se um aplicativo de servidor OLE for um servidor local, o que significa que ele é executado em seu próprio espaço de processo, a comunicação entre o contêiner e o servidor deve ocorrer entre limites de processo. Como esse processo é caro, o OLE depende de um objeto substituto carregado no espaço de processo do contêiner para agir em nome de um aplicativo de servidor local. Esse objeto alternativo, conhecido como *manipulador de objetos*, solicitações de contêiner de serviços que não exigem a atenção do aplicativo de servidor, como solicitações de desenho. Quando um contêiner solicita algo que o manipulador de objetos não pode fornecer, o manipulador se comunica com o aplicativo de servidor usando o mecanismo de comunicação fora do processo do COM.

Um manipulador de objeto é exclusivo de uma classe de objeto. Quando você cria uma instância de um manipulador para uma classe, não pode usá-la para outra. Quando usado para um documento composto, o manipulador de objetos implementa as estruturas de dados do lado do contêiner quando os objetos de uma determinada classe são acessados remotamente.

O OLE fornece um manipulador de objeto padrão que os aplicativos de servidor local podem usar. Para aplicativos que exigem comportamentos especiais, os desenvolvedores podem implementar um manipulador personalizado que substitui o manipulador padrão ou o usa para fornecer determinados comportamentos padrão.

Um manipulador de objeto é uma DLL que contém vários componentes de interação. Esses componentes incluem partes de comunicação remota para gerenciar a comunicação entre o manipulador e seu aplicativo de servidor, um cache para armazenar os dados de um objeto, juntamente com informações sobre como esses dados devem ser formatados e exibidos e um objeto de controle que coordena as atividades dos outros componentes da DLL. Além disso, se um objeto for um link, a DLL também incluirá um componente de vinculação ou *objeto vinculado*, que controla o nome e o local da origem do link.

O *cache* contém dados e informações de apresentação suficientes para que o manipulador exiba um objeto carregado, mas não em execução, em seu contêiner. O OLE fornece uma implementação do cache usado pelo manipulador de objetos padrão do OLE e o objeto de link. O cache armazena dados em formatos necessários para o manipulador de objeto atender às solicitações de desenho de contêiner. Quando os dados de um objeto são alterados, o objeto envia uma notificação ao cache para que uma atualização possa ocorrer. Para obter mais informações sobre o cache, consulte [exibir Caching](view-caching.md).

Para obter mais informações, consulte o tópico a seguir:

-   [O manipulador padrão e os manipuladores personalizados](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> </dl>

 

 




