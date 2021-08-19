---
description: Usando o MS Shell Dlg e o MS Shell Dlg 2
ms.assetid: ac3b57a6-5b92-4366-ad71-c501cec60997
title: Usando o MS Shell Dlg e o MS Shell Dlg 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c29b6f45267ee9f123e5a6dddcd044d667fbe4553af8b3f580edd633b2293ef2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389503"
---
# <a name="using-ms-shell-dlg-and-ms-shell-dlg-2"></a>Usando o MS Shell Dlg e o MS Shell Dlg 2

Windows está disponível em edições localizadas para muitos idiomas. No entanto, a edição em inglês também pode ser usada para executar aplicativos escritos em idiomas diferentes do inglês. Isso é verdadeiro mesmo quando o script usado para esses idiomas é diferente, como quando os aplicativos são escritos em grego ou japonês. Esses aplicativos exigem uma interface do usuário com caixas de diálogo, ícones e utilitários que fornecem informações na linguagem do aplicativo, que podem ser diferentes da linguagem que está sendo usada na interface do usuário Windows atual.

O problema ao selecionar a fonte para uma interface do usuário é óbvio. Por exemplo, a fonte do shell, também conhecida como o sistema ou fonte padrão, para inglês (Estados Unidos) Windows 98 é MS Sans Serif, enquanto a fonte do shell para grego (Grego) Windows 98 é grego MS Sans Serif. Para japonês (Japão) Windows 98, a fonte do shell é MS UI Nova. Esses conjuntos de caracteres não podem ser mapeados diretamente entre si. A substituição de MS Sans Serif por MS Sans Serif grego quando a localidade está definida como grego (Grego) não permite que os aplicativos existentes executem adequadamente ou para exibir caracteres gregos em menus do sistema, caixas de diálogo e controles de edição.

Windows resolve esse problema usando as fontes lógicas MS Shell Dlg e MS Shell Dlg 2 para permitir a seleção da fonte apropriada para exibição de script. Esta seção aborda várias considerações de programação para usar as fontes lógicas para implementar caixas de diálogo, menus e assim por diante para interfaces de usuário flexíveis que são exibidas bem em todos os sistemas operacionais Windows com suporte e em todas as linguagens. Para obter mais informações, consulte [Criação e seleção de fonte.](../gdi/font-creation-and-selection.md) Confira também [Interface de Usuário Multilíngue](multilingual-user-interface.md) para uma discussão sobre o uso da tecnologia Interface de Usuário Multilíngue (MUI) na criação de interfaces do usuário para seus aplicativos multilíngues.

## <a name="about-the-logical-fonts"></a>Sobre as fontes lógicas

As fontes lógicas MS Shell Dlg e MS Shell Dlg 2 são essencialmente nomes de rosto usados para mapeamento para habilitar o suporte para localidades/culturas com caracteres que não estão contidos na página de código 1252, o conjunto de caracteres Windows para o Estados Unidos e a Europa Ocidental. O Dlg do Shell MS é mapeado para a fonte de shell padrão associada à cultura/localidade atual e dá suporte à aparência Windows área de trabalho clássica. O nome facial do MS Shell Dlg 2 foi introduzido no Windows 2000 para dar suporte à aparência que foi introduzida com o Windows 2000.

Por exemplo, se seu aplicativo usar o MS Shell Dlg ou o MS Shell Dlg 2 para suas caixas de diálogo, uma equipe de localização que cria recursos de idioma grego para seu aplicativo poderá se concentrar na tradução de texto. Eles não precisam se preocupar com problemas como a distinção entre MS Sans Serif e MS Sans Serif grego.

> [!Note]  
> As fontes geradas pelo Dlg do MS Shell e pelo MS Shell Dlg 2 são diferentes em diferentes Windows versões. Portanto, você deve garantir que os elementos da interface do usuário são exibidos bem em todas as plataformas.

 

## <a name="handle-hard-coded-font-names"></a>Manipular Hard-Coded de fonte

O uso de Unicode permite que os aplicativos lidam com milhares de caracteres diferentes, mas a maioria das fontes não abrange todo o conjunto de caracteres Unicode. Seus aplicativos não devem codificar nomes de fonte. Um motivo é que codificar um nome de fonte que exibe caracteres para um idioma e não caracteres para outro idioma faz com que todo o texto localizado no segundo idioma seja exibido incorretamente. Outro motivo para não codificar nomes de fonte é que a fonte desejada pode não ser carregada no sistema operacional que está exibindo o texto do aplicativo.

A melhor maneira de tratar nomes de fonte é considerá-los como recursos localizáveis. Usar uma fonte lógica resolve o problema de executar sua interface usando qualquer linguagem Windows NT ou Windows 2000, para qualquer idioma. Definir um nome de fonte como um recurso localizável possibilita que o localizador altere a fonte para a interface do usuário localizada.

## <a name="handle-hard-coded-font-sizes"></a>Manipular Hard-Coded de fonte

Alguns scripts são complexos e exigem um grande número de pixels para exibição correta. Por exemplo, a maioria dos caracteres em inglês é exibida em uma grade 5x7, mas os caracteres em japonês precisam de pelo menos uma grade 16x16 para serem claramente vistos. Enquanto o chinês precisa de uma grade 24x24, o tailandês precisa apenas de 8 pixels de largura, mas pelo menos 22 pixels para altura. É fácil entender que alguns caracteres podem não ser legíveis em um tamanho de fonte pequeno.

A interface do usuário do aplicativo deve tratar os tamanhos de fonte como recursos localizáveis. Usar uma fonte lógica resolve o problema de executar sua interface usando qualquer linguagem Windows NT ou Windows 2000, para qualquer idioma. Definir um tamanho de fonte como um recurso localizável permite que o localizador altere a fonte para a interface do usuário localizada.

## <a name="map-the-logical-fonts"></a>Mapear as fontes lógicas

Cada uma das fontes lógicas é mapeada por uma entrada no Registro para a fonte de shell apropriada para a localidade ativa no momento. Quando uma das fontes lógicas é usada, Windows alterna para a fonte para a localidade selecionada no momento em runtime. Essa operação permite a exibição correta da interface do usuário em inglês (Estados Unidos) Windows, bem como caracteres que não estão na página de código 1252. Portanto, atualmente, o envio de aplicativos localizados pode ser executado na versão Estados Unidos inglês do Windows sem modificação.

Cada computador Windows mapeia o Dlg do MS Shell e o MS Shell Dlg 2 para uma fonte física apropriada, com base no idioma definido para programas não Unicode, descritos na [Terminologia do NLS.](nls-terminology.md) Os mapeamentos reais são armazenados na chave do Registro HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ \\ FontSubstitutes da Versão Atual.

### <a name="font-mapping-on-windows-me9895"></a>Mapeamento de fonte Windows me/98/95

O DLG do Shell MS geralmente é mapeada para uma versão específica da página de código do MS Sans Serif.

### <a name="font-mapping-on-windows-nt-40"></a>Mapeamento de fonte Windows NT 4.0

MS Shell Dlg mapeia para MS Sans Serif para europeu ocidental e central, grego, turco, báltico e idiomas usando script cirílico; MS UI Desemão para japonês; Gulim para coreano; Simsun para chinês simplificado; PMinglu para chinês tradicional; Etc.

### <a name="font-mapping-on-windows-2000-windows-xp-windows-server-2003-windows-vista-and-windows-7"></a>Mapeamento de fonte Windows 2000, Windows XP, Windows Server 2003, Windows Vista e Windows 7

Ambas as fontes lógicas são mapeada para fontes TrueType baseadas em Unicode. O MS Shell Dlg usará o Microsoft Sans Serif (diferente do MS Sans Serif) se o idioma de instalação não for japonês. O Dlg do Shell MS é mapeado para o MS UI Também se o idioma de instalação for japonês.

No Windows XP MUI, o Dlg do MS Shell é mapeável para a Interface do Usuário do MS Somente quando a localidade do sistema e a linguagem de interface do usuário são definidas como japonês. Caso contrário, o Dlg do MS Shell é mapeou para o Microsoft Sans Serif.

No Windows Vista e Windows 7, o Dlg do MS Shell será mapeado para a Interface do Usuário do MS Se a linguagem de interface do usuário padrão do computador estiver definida como japonês (independentemente do idioma de instalação). O Dlg do Shell MS será mapeado para o Microsoft Sans Serif se a linguagem de interface do usuário padrão do computador estiver definida como um idioma diferente do japonês.

O MS Shell Dlg 2 simplesmente usa a fonte Toma, independentemente do idioma. A principal vantagem do Toma em relação ao Microsoft Sans Serif é que o Toma tem um rosto de fonte em negrito nativo. Sua principal desvantagem é que sistemas operacionais mais antigos podem não ter instalado e podem substituir uma fonte menos atraente.

Os caracteres que não são implementados no Toma ou no Microsoft Sans Serif podem ser implementados em outras fontes Windows que são usadas para exibição de texto em interfaces do usuário. Dependendo de quais controles ou APIs são usados [](https://msdn.microsoft.com/globalization/mt662331) para exibir texto, vários mecanismos como vinculação de fonte podem ser usados pelo sistema para selecionar automaticamente essas fontes para exibir esses caracteres.

Os aplicativos podem usar o Microsoft Sans Serif ou o Toma explicitamente e salvar o nível de indulgidade envolvido no uso do Dlg do MS Shell ou do MS Shell Dlg 2. Devido à vinculação de fonte, especificar Microsoft Sans Serif ou Toma fornece glifos apropriados para todos os idiomas.

## <a name="use-ms-shell-dlg-for-a-non-english-application-on-windows-me9895"></a>Usar o Dlg do MS Shell para um aplicativo que não seja inglês Windows Me/98/95

No Windows Me/98/95, o Dlg do MS Shell não se destina ao uso com um aplicativo de interface do usuário estático não inglês que é executado quando o usuário escolheu uma localidade com um conjunto de caracteres base Windows diferente. Nesse caso, a linguagem de interface do usuário do aplicativo pode não ter suporte com a fonte que é substituída pelo MS Shell Dlg.

Por exemplo, se o usuário estiver usando uma versão de idioma alemão do Windows e quiser instalar um aplicativo de idioma grego não Unicode, o usuário tentará alterar a localidade para grego (Grego). Essa ação redefine o Dlg do MS Shell para uma fonte grego, mas essa fonte não contém todos os glifos necessários para exibição em alemão. Portanto, os caracteres não ASCII na interface do usuário do idioma alemão não serão exibidos corretamente. Para dar suporte a esse cenário, um aplicativo precisa definir o Dlg do MS Shell como uma fonte que contém os glifos europeus e gregos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumeração e seleção de fontes internacionais](using-international-fonts-and-text.md)
</dt> <dt>

[Interface do Usuário Multilíngue](multilingual-user-interface.md)
</dt> </dl>

 

 
