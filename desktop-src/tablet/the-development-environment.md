---
description: Você não precisa de um tablet para desenvolver aplicativos de Tablet PC, mas precisa de um computador pessoal capaz de executar o software listado posteriormente neste tópico.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: O Ambiente de Desenvolvimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d6c0de35fa84ec4ee01b3f25aaefec6ab3470fde83161f7aaf2157197bbf1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449209"
---
# <a name="the-development-environment"></a>O Ambiente de Desenvolvimento

Você não precisa de um tablet para desenvolver aplicativos de Tablet PC, mas precisa de um computador pessoal capaz de executar o software listado posteriormente neste tópico.

É fortemente recomendável que você teste seu aplicativo em um tablet pc real para garantir que todas as diferenças no hardware, como o digitalizador de resolução mais alta, sejam contabilizados.

Um sistema de desenvolvimento mínimo típico consiste no hardware e software a seguir.

## <a name="hardware"></a>Hardware

-   8 MB de espaço em disco rígido para uma instalação completa.
-   Um dispositivo que aponta para entrada. Isso inclui dispositivos como um mouse, um tablet externo ou um tablet com um digitalizador HID.

HID significa dispositivos de interface humana, um padrão para dispositivos de entrada. Os digitalizadores em conformidade com HID são tratados como um mouse normal, enquanto os digitalizadores em conformidade com HID têm maior resolução e mais metadados em traços, como pressão, semelhantes aos instalados no hardware do Tablet PC.

## <a name="software"></a>Software

Os seguintes sistemas operacionais podem ser usados para desenvolver aplicativos de Tablet PC:

-   Windows 7
-   Windows Vista
-   Windows Server 2008
-   Windows XP Tablet PC Edition 2005
-   Windows Server 2003
-   Windows XP Professional

Você também precisará de:

-   Visual Studio versão 6 com Service Pack 5 ou Visual Studio .NET ou Visual Studio .NET 2005
-   Microsoft Internet Explorer 6 ou superior (recomendado)

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a>Detalhes sobre como desenvolver SKUs de computadores não tablets Windows

Os componentes da plataforma tablet PC podem ser instalados no Windows XP Professional com Service Pack 2 ou Windows Server 2003. Nesses sistemas operacionais, seu aplicativo pode coletar tinta com a [**classe InkCollector**](inkcollector-class.md) e pode ser testado e depurado. No entanto, nenhum reconhecimento está disponível, a menos que você também instale o Microsoft Windows XP Tablet PC Edition 2005 Recognizer Pack. Você pode baixar esse pacote no Centro de Download no MSDN.

Depois de instalar o SDK do Windows em um sistema do Windows XP Professional ou Windows Server 2003, você terá todos os arquivos de desenvolvimento necessários para criar aplicativos de tinta (como msinkaut.h para um desenvolvedor COM). No entanto, você não poderá executar ou depurar seu aplicativo nesse sistema até instalar os arquivos de runtime. Por exemplo, no caso de um desenvolvedor COM, inkobj.dll deve ser instalado e registrado. Como você não está em um sistema em que esses arquivos de plataforma existem, você deve instalar os componentes da plataforma Tablet PC do módulo de mesclagem redistribuível, mstpcrt.msm, para obter os arquivos de runtime em seu sistema.

A maneira mais simples de instalar os runtimes de plataforma em um sistema do Windows XP Professional ou Windows 2000 para fins de desenvolvimento é compilar o projeto de configuração de exemplo fornecido com os Exemplos de PC Móvel e Tablet PC e implantá-lo no computador de desenvolvimento.

> [!Note]  
> Windows O Vista e Windows XP Tablet PC Edition 2005 já têm os componentes da plataforma instalados, portanto, eles não exigem etapas adicionais para executar e depurar aplicativos de tablet pc.

 

Os controles [InkEdit](inkedit-control-reference.md) e [InkPicture](inkpicture-control-reference.md) podem ser usados para coletar tinta no Windows 2000 com Service Pack 4 ou Windows XP Professional com Service Pack 2 quando os componentes da plataforma tablet pc estão presentes instalando o SDK do Tablet PC versão 1.7, mas não são capazes de coletar tinta em sistemas de pc não Tablet que não têm os componentes da plataforma tablet PC instalados.

O Windows SDK fornece todos os componentes necessários para desenvolver aplicativos de Tablet PC em SKUs não Tablet de Windows. De definir a seguinte chave do Registro **DWORD** como 1 para coletar tinta em SKUs não Tablet de Windows:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

Essa chave destina-se apenas a fins de desenvolvimento.

 

 



