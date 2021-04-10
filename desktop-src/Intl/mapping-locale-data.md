---
description: O NLS inclui várias funções de API que seus aplicativos podem usar para mapear dados de localidade entre identificadores de localidade e nomes de localidade e listar localidades neutras.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Mapeando dados de localidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164835"
---
# <a name="mapping-locale-data"></a>Mapeando dados de localidade

O NLS inclui várias funções de API que seus aplicativos podem usar para mapear dados de localidade entre [identificadores de localidade](locale-identifiers.md) e [nomes de localidade](locale-names.md)e listar localidades neutras. Este tópico aborda o uso dessas funções no Windows Vista e posterior e em sistemas operacionais anteriores ao Windows Vista (às vezes chamados de "sistemas de nível inferior").

## <a name="map-locale-data-on-windows-vista-and-later"></a>Mapear dados de localidade no Windows Vista e posterior

O NLS fornece várias funções de mapeamento de localidade para uso por aplicativos que você desenvolve para executar no Windows Vista e versões posteriores. Ele também inclui funções que seus aplicativos podem usar para enumerar localidades neutras.

**Usar as funções de conversão padrão para mapeamento de dados**

Para mapear entre um nome de localidade e um identificador de localidade, seu aplicativo pode chamar a função [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) . O aplicativo usa [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) para mapear entre um identificador de localidade e um nome de localidade.

**Listar localidades neutras**

Para enumerar localidades neutras para o Windows 7 e posterior, seu aplicativo pode chamar [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) com *dwFlags* definido como [**locale \_ NEUTRALDATA**](locale-neutraldata.md). Ele também pode usar [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) com *LCTYPE* definido como [**localidade \_ INEUTRAL**](locale-ineutral.md).

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a>Mapear dados de localidade em sistemas operacionais anteriores ao Windows Vista

O NLS inclui uma DLL (biblioteca de vínculo direto) a ser usada para aplicativos que você desenvolve para execução em sistemas operacionais anteriores ao Windows Vista. A DLL dá suporte às funções de conversão e listagem para mapeamento de dados.

> [!Note]  
> Os aplicativos que só são executados no Windows Vista e posterior não devem usar o mapeamento de nível inferior ou as funções de listagem.

 

**Usar as funções de conversão de nível inferior para mapeamento de dados**

Seu aplicativo direcionado a um sistema de nível inferior pode chamar a função [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) para converter um identificador de localidade em um nome de localidade. Se precisar converter um nome de localidade em um identificador de localidade, ele deverá chamar [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).

**Usar as funções de listagem de nível inferior para enumerar localidades neutras**

Seu aplicativo deve chamar o [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) para recuperar o identificador de localidade do pai para uma localidade. Se o aplicativo precisar obter o nome da localidade do pai para a localidade, ele deverá chamar [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o suporte ao idioma nacional](using-national-language-support.md)
</dt> <dt>

[Identificadores de localidade](locale-identifiers.md)
</dt> <dt>

[Nomes de localidade](locale-names.md)
</dt> </dl>

 

 



