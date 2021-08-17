---
description: O NLS inclui várias funções de API que seus aplicativos podem usar para mapear dados de localidade entre identificadores de localidade e nomes de localidade e listar localidades neutras.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Mapeando dados de localidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1576844f13dda80a6b9d754fc807ef8a35514dcfedd88dc04cf233cfb2a1bfb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147180"
---
# <a name="mapping-locale-data"></a>Mapeando dados de localidade

O NLS inclui várias funções de API que seus aplicativos [](locale-identifiers.md) podem usar [](locale-names.md)para mapear dados de localidade entre identificadores de localidade e nomes de localidade e listar localidades neutras. Este tópico discute o uso dessas funções no Windows Vista e posterior e em sistemas operacionais Windows Vista pré-Windows (às vezes chamados de "sistemas de nível baixo").

## <a name="map-locale-data-on-windows-vista-and-later"></a>Mapear dados de localidade no Windows Vista e posterior

O NLS fornece várias funções de mapeamento de localidade para uso por aplicativos que você desenvolve para executar no Windows Vista e posterior. Ele também inclui funções que seus aplicativos podem usar para enumerar localidades neutras.

**Usar as funções de conversão padrão para mapeamento de dados**

Para mapear entre um nome de localidade e um identificador de localidade, seu aplicativo pode chamar a [**função LocaleNameToLCID.**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) O aplicativo usa [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) para mapear entre um identificador de localidade e um nome de localidade.

**Listar localidades neutras**

Para enumerar localidades neutras para Windows 7 e posteriores, seu aplicativo pode chamar [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) com *dwFlags* definido como [**LOCALE \_ NEUTRALDATA.**](locale-neutraldata.md) Ele também pode usar [**GetLocaleInfoEx com**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) *LCType* definido como [**LOCALE \_ INEUTRAL.**](locale-ineutral.md)

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a>Mapear dados de localidade em sistemas operacionais Windows Vista pré-Windows

O NLS inclui uma DLL (biblioteca de vínculo direto) a ser usada para aplicativos que você desenvolve para executar em sistemas operacionais Windows Vista. A DLL dá suporte a funções de conversão e listagem para mapeamento de dados.

> [!Note]  
> Os aplicativos que são executados Windows Vista e posterior não devem usar as funções de mapeamento ou listagem de nível baixo.

 

**Usar as funções de conversão de nível baixo para mapeamento de dados**

Seu aplicativo direcionado a um sistema de nível baixo pode chamar a função [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) para converter um identificador de localidade em um nome de localidade. Se precisar converter um nome de localidade em um identificador de localidade, ele deverá chamar [**DownlevelLocaleNameToLCID.**](downlevellocalenametolcid.md)

**Usar as funções de listagem de nível baixo para enumerar localidades neutras**

Seu aplicativo deve chamar [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) para recuperar o identificador de localidade do pai para uma localidade. Se o aplicativo precisar obter o nome da localidade do pai para a localidade, ele deverá chamar [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o suporte a idiomas nacionais](using-national-language-support.md)
</dt> <dt>

[Identificadores de localidade](locale-identifiers.md)
</dt> <dt>

[Nomes de localidade](locale-names.md)
</dt> </dl>

 

 



