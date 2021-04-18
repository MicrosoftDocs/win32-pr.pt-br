---
description: Usando MS Shell Dlg e MS Shell Dlg 2
ms.assetid: ac3b57a6-5b92-4366-ad71-c501cec60997
title: Usando MS Shell Dlg e MS Shell Dlg 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad43f972e776151551fa312ce2bd8ed6d19be58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767786"
---
# <a name="using-ms-shell-dlg-and-ms-shell-dlg-2"></a>Usando MS Shell Dlg e MS Shell Dlg 2

O Windows está disponível em edições localizadas para vários idiomas. No entanto, a edição em Inglês-idioma também pode ser usada para executar aplicativos escritos em linguagens diferentes do inglês. Isso é verdadeiro mesmo quando o script usado para esses idiomas é diferente, como quando os aplicativos são escritos em grego ou japonês. Esses aplicativos exigem uma interface do usuário com caixas de diálogo, ícones e utilitários que fornecem informações no idioma do aplicativo, o que pode ser diferente do idioma que está sendo usado na interface do usuário atual do Windows.

O problema na seleção da fonte de uma interface do usuário é óbvio. Por exemplo, a fonte do Shell, também conhecida como a fonte do sistema ou padrão, para inglês (Estados Unidos) Windows 98 é MS Sans Serif, enquanto a fonte do Shell para grego (Grécia) Windows 98 é MS Sans Serif grego. Para japonês (Japão) Windows 98, a fonte do Shell é MS UI Gothic. Esses conjuntos de caracteres não podem ser mapeados diretamente um ao outro. Substituir MS Sans Serif por MS Sans Serif grego quando a localidade é definida como grego (Grécia) não permite que aplicativos existentes sejam executados adequadamente ou que exibam caracteres gregos em menus do sistema, caixas de diálogo e controles de edição.

O Windows resolve esse problema usando as fontes lógicas MS Shell Dlg e MS Shell Dlg 2 para permitir a seleção da fonte apropriada para exibição de script. Esta seção aborda várias considerações de programação para usar as fontes lógicas para implementar caixas de diálogo, menus e o como para interfaces de usuário flexíveis que exibem bem em todos os sistemas operacionais Windows com suporte e em todos os idiomas. Para obter mais informações, consulte [criação e seleção de fontes](../gdi/font-creation-and-selection.md). Consulte também [interface do usuário multilíngue](multilingual-user-interface.md) para obter uma discussão sobre o uso da tecnologia MUI (Multilingual User interface) na criação de interfaces do usuário para seus aplicativos multilíngües.

## <a name="about-the-logical-fonts"></a>Sobre as fontes lógicas

As fontes lógicas MS Shell Dlg e MS Shell Dlg 2 são essencialmente nomes de face usados para mapeamento para habilitar o suporte para localidades/culturas com caracteres que não estão contidos na página de código 1252, o conjunto de caracteres do Windows para o Estados Unidos e Europa Ocidental. O MS Shell Dlg é mapeado para a fonte de shell padrão associada à cultura/localidade atual e dá suporte à aparência clássica da área de trabalho do Windows. O nome da face MS Shell Dlg 2 foi introduzido no Windows 2000 para dar suporte à aparência que foi introduzida com o Windows 2000.

Por exemplo, se seu aplicativo usa MS Shell Dlg ou MS Shell Dlg 2 para suas caixas de diálogo, uma equipe de localização criando recursos de idioma grego para seu aplicativo pode se concentrar na tradução de texto. Eles não precisam se preocupar com problemas como a distinção entre MS Sans Serif e MS Sans Serif grego.

> [!Note]  
> As fontes geradas por MS Shell Dlg e MS Shell Dlg 2 são diferentes em versões diferentes do Windows. Portanto, você deve garantir que os elementos da interface do usuário sejam exibidos bem em todas as plataformas.

 

## <a name="handle-hard-coded-font-names"></a>Manipular Hard-Coded nomes de fonte

O uso de Unicode permite que os aplicativos lidem com milhares de caracteres diferentes, mas a maioria das fontes não cobre todo o conjunto de caracteres Unicode. Seus aplicativos não devem embutir nomes de fontes. Um dos motivos é que embutir um nome de fonte que exibe caracteres para um idioma e não caracteres para outro idioma faz com que todo o texto localizado no segundo idioma seja exibido incorretamente. Outro motivo para não embutir em código os nomes de fontes é que a fonte desejada pode não ser carregada no sistema operacional que está exibindo o texto do aplicativo.

A melhor maneira de tratar os nomes das fontes é considerá-los como recursos localizáveis. O uso de uma fonte lógica resolve o problema de execução da interface usando qualquer linguagem no Windows NT ou no Windows 2000, para qualquer linguagem. Definir um nome de fonte como um recurso localizável possibilita que o localizador altere a fonte da interface do usuário localizada.

## <a name="handle-hard-coded-font-sizes"></a>Manipular Hard-Coded tamanhos de fonte

Alguns scripts são complexos e exigem um grande número de pixels para serem exibidos corretamente. Por exemplo, a maioria dos caracteres em inglês é exibida em uma grade 5x7, mas os caracteres japoneses precisam de pelo menos uma grade de 16x16 para serem vistos claramente. Enquanto o chinês precisa de uma grade 24x24, o tailandês precisa apenas de 8 pixels para largura, mas pelo menos 22 pixels para altura. É fácil entender que alguns caracteres podem não ser legíveis em um tamanho de fonte pequeno.

A interface do usuário do aplicativo deve tratar tamanhos de fonte como recursos localizáveis. O uso de uma fonte lógica resolve o problema de execução da interface usando qualquer linguagem no Windows NT ou no Windows 2000, para qualquer linguagem. Definir um tamanho de fonte como um recurso localizável permite que o localizador altere a fonte da interface do usuário localizada.

## <a name="map-the-logical-fonts"></a>Mapear as fontes lógicas

Cada uma das fontes lógicas é mapeada por uma entrada no registro para a fonte de shell apropriada para a localidade ativa no momento. Quando uma das fontes lógicas é usada, o Windows alterna para a fonte da localidade selecionada no momento em tempo de execução. Essa operação permite a exibição correta da interface do usuário do Windows em inglês (Estados Unidos), bem como os caracteres que não estão na página de código 1252. Assim, o envio de aplicativos localizados no momento pode ser executado na versão em inglês (Estados Unidos) do Windows sem modificação.

Cada computador com Windows mapeia MS Shell Dlg e MS Shell Dlg 2 para uma fonte física apropriada, com base na linguagem definida para programas não-Unicode, descritas na [terminologia do NLS](nls-terminology.md). Os mapeamentos reais são armazenados na chave do registro HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ atual versão \\ FontSubstitutes.

### <a name="font-mapping-on-windows-me9895"></a>Mapeamento de fontes no Windows me/98/95

O MS Shell Dlg geralmente é mapeado para uma versão específica de página de código de MS Sans Serif.

### <a name="font-mapping-on-windows-nt-40"></a>Mapeamento de fontes no Windows NT 4,0

MS Shell Dlg é mapeado para MS Sans Serif para Europa Ocidental e central, grego, turco, Báltico e idiomas usando o script cirílico; MS UI Gothic para japonês; Gulim para coreano; SimSun para chinês simplificado; PMinglu para chinês tradicional; diante.

### <a name="font-mapping-on-windows-2000-windows-xp-windows-server-2003-windows-vista-and-windows-7"></a>Mapeamento de fontes no Windows 2000, Windows XP, Windows Server 2003, Windows Vista e Windows 7

Ambas as fontes lógicas são mapeadas para fontes TrueType baseadas em Unicode. O MS Shell Dlg usa a Microsoft Sans Serif (DISTINCT de MS Sans Serif) se o idioma de instalação não estiver em Japonês. MS Shell Dlg é mapeado para MS UI Gothic se o idioma de instalação for japonês.

Em sistemas MUI do Windows XP, o MS Shell Dlg é mapeado para MS UI Gothic somente quando a localidade do sistema e o idioma da interface do usuário são definidos para japonês. Caso contrário, MS Shell Dlg é mapeado para o Microsoft Sans Serif.

No Windows Vista e no Windows 7, o MS Shell Dlg é mapeado para o MS UI Gothic se o idioma padrão da interface do usuário do computador estiver definido como japonês (independentemente do idioma de instalação). O MS Shell Dlg é mapeado para o Microsoft Sans Serif se o idioma padrão da interface do usuário do computador estiver definido como um idioma diferente do japonês.

O MS Shell Dlg 2 simplesmente usa a fonte Tahoma, independentemente da linguagem. A principal vantagem do Tahoma em relação ao Microsoft Sans Serif é que Tahoma tem uma face de fonte em negrito nativa. Sua principal desvantagem é que sistemas operacionais mais antigos podem não ter sido instalados e podem substituir uma fonte menos atraente.

Os caracteres que não são implementados em Tahoma ou Microsoft Sans Serif podem ser implementados em outras fontes do Windows que são usadas para exibição de texto em interfaces do usuário. Dependendo de quais controles ou APIs são usados para exibir texto, vários mecanismos, como a [vinculação de fontes](https://msdn.microsoft.com/globalization/mt662331) , podem ser usados pelo sistema para selecionar automaticamente essas fontes para exibição desses caracteres.

Os aplicativos podem usar a Microsoft Sans Serif ou Tahoma explicitamente e salvar o nível de indireção envolvido no uso do MS Shell Dlg ou MS Shell Dlg 2. Devido à vinculação de fontes, a especificação de Microsoft Sans Serif ou Tahoma fornece glifos apropriados para todos os idiomas.

## <a name="use-ms-shell-dlg-for-a-non-english-application-on-windows-me9895"></a>Usar o MS Shell Dlg para um aplicativo que não esteja em inglês no Windows me/98/95

No Windows me/98/95, o MS Shell Dlg não se destina ao uso com um aplicativo de interface do usuário estático e não inglês que é executado quando o usuário escolhe uma localidade com um conjunto de caracteres base do Windows diferente. Nesse caso, o idioma da interface do usuário do aplicativo pode não ter suporte com a fonte substituída por MS Shell Dlg.

Por exemplo, se o usuário estiver usando uma versão em idioma alemão do Windows e quiser instalar um aplicativo não Unicode em idioma grego, o usuário tentará alterar a localidade para grego (Grécia). Essa ação redefine o MS Shell Dlg para uma fonte em grego, mas essa fonte não contém todos os glifos necessários para serem exibidos em alemão. Portanto, quaisquer caracteres não-ASCII na interface do usuário do idioma alemão não serão exibidos corretamente. Para dar suporte a esse cenário, um aplicativo precisa definir o MS Shell Dlg para uma fonte que contenha os glifos da Europa Ocidental e do grego.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Seleção e enumeração de fontes internacionais](using-international-fonts-and-text.md)
</dt> <dt>

[Interface do Usuário Multilíngue](multilingual-user-interface.md)
</dt> </dl>

 

 
