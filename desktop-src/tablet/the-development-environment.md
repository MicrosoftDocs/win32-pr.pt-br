---
description: Você não precisa de um Tablet PC para desenvolver aplicativos de Tablet PC, mas precisa de um computador pessoal capaz de executar o software listado posteriormente neste tópico.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: O ambiente de desenvolvimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefa29a518beaf21aa8b2457abf17d9581075f73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922834"
---
# <a name="the-development-environment"></a>O ambiente de desenvolvimento

Você não precisa de um Tablet PC para desenvolver aplicativos de Tablet PC, mas precisa de um computador pessoal capaz de executar o software listado posteriormente neste tópico.

É altamente recomendável que você teste seu aplicativo em um Tablet PC real para garantir que todas as diferenças no hardware, como o digitalizador de resolução mais alta, sejam contadas para o.

Um sistema comum de desenvolvimento mínimo consiste no hardware e software a seguir.

## <a name="hardware"></a>Hardware

-   8 MB de espaço em disco rígido para uma instalação completa.
-   Um dispositivo apontador para entrada. Isso inclui dispositivos como um mouse, um Tablet externo ou um Tablet PC com um digitalizador HID.

O HID significa dispositivos de interface humana, um padrão para dispositivos de entrada. Os digitalizadores não compatíveis com HID são tratados como um mouse regular, enquanto os digitalizadores compatíveis com HID têm resolução maior e mais metadados em traços, como pressão, semelhantes aos que estão instalados no hardware do Tablet PC.

## <a name="software"></a>Software

Os seguintes sistemas operacionais podem ser usados para desenvolver aplicativos para Tablet PC:

-   Windows 7
-   Windows Vista
-   Windows Server 2008
-   Windows XP Tablet PC Edition 2005
-   Windows Server 2003
-   Windows XP Professional

Você também precisará de:

-   Visual Studio versão 6 com Service Pack 5, ou Visual Studio .NET ou Visual Studio .NET 2005
-   Microsoft Internet Explorer 6 ou superior (recomendado)

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a>Detalhes sobre o desenvolvimento em SKUs sem Tablet PC do Windows

Os componentes da plataforma Tablet PC podem ser instalados no Windows XP Professional com Service Pack 2 ou no Windows Server 2003. Nesses sistemas operacionais, seu aplicativo pode coletar tinta com a classe [**InkCollector**](inkcollector-class.md) e pode ser testado e depurado. No entanto, nenhum reconhecimento estará disponível a menos que você também instale o pacote de reconhecimento do Microsoft Windows XP Tablet PC Edition 2005. Você pode baixar esse pacote do centro de download no MSDN.

Depois de instalar o SDK do Windows em um sistema Windows XP Professional ou Windows Server 2003, você terá todos os arquivos de desenvolvimento necessários para criar aplicativos de tinta (como msinkaut. h para um desenvolvedor COM). No entanto, você não poderá executar ou depurar seu aplicativo nesse sistema até instalar os arquivos de tempo de execução. Por exemplo, no caso de um desenvolvedor COM, inkobj.dll deve ser instalado e registrado. Como você não está em um sistema onde esses arquivos de plataforma existem, você deve instalar os componentes da plataforma Tablet PC do módulo de mesclagem redistribuível, mstpcrt. msm, para obter os arquivos de tempo de execução em seu sistema.

A maneira mais simples de obter os tempos de execução da plataforma instalados em um sistema Windows XP Professional ou Windows 2000 para fins de desenvolvimento é compilar o projeto de configuração de exemplo fornecido com os exemplos de PC móvel e Tablet PC e implantá-lo no computador de desenvolvimento.

> [!Note]  
> O Windows Vista e o Windows XP Tablet PC Edition 2005 já têm os componentes da plataforma instalados, portanto, eles não exigem etapas adicionais para executar e depurar aplicativos do Tablet PC.

 

Os controles [InkEdit](inkedit-control-reference.md) e [InkPicture](inkpicture-control-reference.md) podem ser usados para coletar tinta no Windows 2000 com Service Pack 4 ou Windows XP Professional com Service Pack 2 quando os componentes da plataforma do Tablet PC estão presentes, instalando o SDK do Tablet PC versão 1,7, mas não podem coletar tinta em sistemas que não são do Tablet PC que não têm os componentes da plataforma Tablet PC instalados.

O SDK do Windows fornece todos os componentes necessários para desenvolver aplicativos para Tablet PC em SKUs não-Tablet do Windows. Defina a seguinte chave do registro **DWORD** como 1 para coletar tinta em SKUs não-Tablet do Windows:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

Essa chave destina-se apenas a fins de desenvolvimento.

 

 



