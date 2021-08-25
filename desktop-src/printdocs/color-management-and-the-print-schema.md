---
description: Saiba mais sobre palavras-chave configuráveis pelo usuário no esquema de impressão para gerenciamento de cores, como PageColorManagement e PageBlackGenerationProcessing.
ms.assetid: 296255b8-fe5c-46dd-b717-487aaae0db80
title: Gerenciamento de cores e o esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e7e5a86b9f598183a4b3765e1cc38836b4ee7bb62e1835e06575392771dc5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846377"
---
# <a name="color-management-and-the-print-schema"></a>Gerenciamento de cores e o esquema de impressão

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

As palavras-chave do elemento configurável pelo usuário podem ser específicas de XPS ou específicas não-XPS. No caso em que eles não são específicos do XPS, a palavra-chave pode ser usada para impressão baseada em GDI herdada. Se um aplicativo decidir definir essas palavras-chave em um PrintTicket, cabe ao driver determinar a ação e o comportamento adequados a serem tomadas com base nas definições apresentadas no esquema de impressão. Qualquer uma dessas palavras-chave pode ser usada no contexto de ICM. para obter mais informações, consulte o SDK do Windows Vista.



| Palavra-chave configurável do usuário do esquema de impressão       | DEVMODE equivalente     | Específico do XPS   |
|----------------------------------------------|------------------------|----------------|
| PageColorManagement<br/>               | dmICMMethod<br/> | Não<br/>  |
| PageBlackGenerationProcessing<br/>     | Nenhum<br/>        | Sim<br/> |
| PageBlendColorSpace<br/>               | Nenhum<br/>        | Sim<br/> |
| PageSourceColorProfile<br/>            | Nenhum<br/>        | Não<br/>  |
| PageDestinationColorProfile<br/>       | Nenhum<br/>        | Não<br/>  |
| PageICMRenderingIntent<br/>            | dmICMIntent<br/> | Não<br/>  |
| JobOptimalDestinationColorProfile<br/> | Nenhum<br/>        | Não<br/>  |
| PageDeviceColorSpaceUsage<br/>         | Nenhum<br/>        | Sim<br/> |



 

## <a name="pagecolormanagement-system-handling"></a>Manipulação do sistema PageColorManagement

Para PageColorManagement, o sistema fornece manipulação automática de PrintTicket para DEVMODE ou DEVMODE para conversão de PrintTicket, se necessário. Isso depende do caminho de impressão específico entre o aplicativo (Win32 ou WPF) e o driver (baseado em GDI ou XPSDrv). no caso de impressão de um aplicativo Windows Presentation Foundation para um driver de impressão XPSDrv da Microsoft, uma opção pública PageColorManagement do sistema não deve ser anunciada no documento PrintTicket ou printcapabilities; Nesse caso, o gerenciamento de cores não pode ser manipulado automaticamente pelo sistema. A impressão de um aplicativo Win32 para um driver de impressão XPSDrv da Microsoft pode resultar em gerenciamento de cores entre o aplicativo e o GDI, no entanto, após a conversão para o formato XPS, não haverá manipulação automática do sistema de gerenciamento de cores entre o documento XPS e o driver e/ou o dispositivo, pois o formato XPS marca cada elemento com informações de cores completas e cabe ao driver ou dispositivo processar essas informações.



| Opções públicas do PageColorManagement | Valor de DEVMODE                  |
|------------------------------------|--------------------------------|
| Nenhum<br/>                    | DMICMMETHOD \_ nenhum<br/>   |
| Dispositivo<br/>                  | \_dispositivo DMICMMETHOD<br/> |
| Driver<br/>                  | \_Driver DMICMMETHOD<br/> |
| Sistema<br/>                  | \_sistema DMICMMETHOD<br/> |



 

## <a name="pageicmrenderingintent-system-handling"></a>Manipulação do sistema PageICMRenderingIntent

Para PageICMRenderingIntent, o sistema fornece manipulação automática de PrintTicket para DEVMODE ou DEVMODE para conversão de PrintTicket, se necessário. isso depende do caminho de impressão específico entre o aplicativo (Win32 ou Windows Presentation Foundation) e o driver (baseado em GDI ou XPSDrv).



| Opções públicas do PageICMRenderingIntent | Valor de DEVMODE                       |
|---------------------------------------|-------------------------------------|
| AbsoluteColorimetric<br/>       | colorimétrico DMICM do \_ ABS \_<br/> |
| RelativeColorimetric<br/>       | \_COLORIMÉTRICO DMICM<br/>      |
| Fotografias<br/>                | contraste de DMICM \_<br/>          |
| BusinessGraphics<br/>           | \_saturação DMICM<br/>          |



 

Todas as outras palavras-chave relacionadas ao gerenciamento de cores (além de PageColorManagement ou PageICMRenderingIntent) não têm tal manipulação automática.

## <a name="joboptimaldestinationcolorprofile-and-pagedestinationcolorprofile-usage"></a>Uso de JobOptimalDestinationColorProfile e PageDestinationColorProfile

Um aplicativo pode decidir consultar o documento de PrintCapabilities para JobOptimalDestinationColorProfile. Isso pode dar a um aplicativo o perfil de cor ideal, considerando a configuração atual do dispositivo, conforme definido no documento PrintCapabilities. Se o aplicativo decidir que o driver executa o gerenciamento de cores para o perfil de cor de destino especificado por JobOptimalDestinationColorProfile, PageColorManagement e PageDestinationColorProfile seriam definidos como driver e DriverConfiguration no PrintTicket, respectivamente. Se o aplicativo não quiser usar o JobOptionalDestinationColorProfile e optar por usar seu próprio, ele deverá definir PageColorManagement como None e também definir o PageDestinationColorProfile como aplicativo no PrintTicket para transmitir que o aplicativo já realizou o gerenciamento de cores para seu perfil de cor de destino especificado. Outro cenário pode ocorrer quando o aplicativo opta por usar o perfil de cor de destino ideal retornado pelos drivers de PrintCapabilities, mas decide fazer o gerenciamento de cores por conta própria. Nesse caso, PageColorManagement seria definido como None e PageDestinationColorProfile seria definido como Application.

## <a name="pagesourcecolorprofile-usage"></a>Uso de PageSourceColorProfile

Para PageSourceColorProfile, um aplicativo pode especificar um perfil de cor de origem para cada página no PrintTicket, independentemente da opção selecionada para PageColorManagement. Independentemente de estar presente ou não, cabe ao driver decidir o comportamento de cada caso com base nas definições apresentadas no esquema de impressão. Por exemplo, um aplicativo pode definir PageColorManagement como nenhum e, em seguida, não definir PageSourceColorProfile no PrintTicket. Também é possível que um aplicativo defina PageColorManagement para driver e, em seguida, defina PageSourceColorProfile no PrintTicket; o driver, nesse caso, é responsável por determinar o comportamento dentro das diretrizes do coesquema.

## <a name="pagedevicecolorspaceusage"></a>PageDeviceColorSpaceUsage

PageDeviceColorSpaceUsage é um elemento que pode ser configurado pelo usuário específico do XPS que é definido pelo aplicativo. Ele fornece instruções para o dispositivo definindo a opção apropriada no PrintTicket, para o tratamento de perfil de espaço de cores associado em um documento XPS. O aplicativo e/ou PrintTicket existente podem especificar essa palavra-chave em um PrintTicket enviado ao dispositivo. Independentemente de estar presente ou não, cabe ao driver decidir o comportamento de cada caso, com base nas definições apresentadas no esquema de impressão.

## <a name="print-schema-color-management-example-flow"></a>Exemplo de gerenciamento de cores do esquema de impressão Flow

O diagrama a seguir ilustra o Flow para os cenários mais prováveis para usar o gerenciamento de cores e o esquema de impressão. Para simplificar e facilitar a legibilidade, somente as seguintes palavras-chave de esquema de impressão configuráveis pelo usuário foram usadas para demonstrar seu uso: PageColorManagement, JobOptimalDestinaionColorProfile, PageSourceColorProfile e PageDestinationColorProfile. Uma linha sólida representa uma ação que deve ocorrer e uma linha tracejada representa uma ação que pode ocorrer. O cenário a seguir não é a interação garantida que resultará entre o aplicativo, o driver e o sistema, no entanto, representa o caso de uso mais comum que ocorrerá.

![um diagrama que mostra como as configurações de gerenciamento de cores são processadas](images/local-1992284846-colormanagementtest3.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




