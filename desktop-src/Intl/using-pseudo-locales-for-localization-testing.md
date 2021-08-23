---
description: no Windows Vista e posterior, você pode usar pseudo-locais para testar a possibilidade de localização de aplicativos. Este tópico inclui procedimentos para usar pseudodispositivos.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Usando pseudo-locais para teste de possibilidade de localização
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: 72d84cbf324823a814c9412580b033792b0d1c8a45630bf2f4cb26dd8b2a1acf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631716"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a>Usando pseudo-locais para teste de possibilidade de localização

as [pseudovariáveis](pseudo-locales.md) são internas para Windows Vista e posterior, para que você possa acessá-las por meio de APIs NLS (suporte a idioma nacional). Você pode usar pseudo-locais para testar a [possibilidade de localização](/windows/uwp/design/globalizing/globalizing-portal) de seus aplicativos. Este tópico inclui procedimentos para usar pseudodispositivos.

> [!NOTE]
> Uma tarefa que precisa de consideração especial quando se trata de pseudo-locais é enumerando-as; seja em seu código ou na parte das opções regionais e de idioma do painel de controle. Mais informações sobre isso posteriormente neste tópico.

Os nomes dos pseudo locais são "qps-ploc", "qps-ploca" e "qps-plocm". a partir de Windows 10, a pseudo-localidade "qps-Latn-x-sh" também está disponível.

## <a name="retrieve-information-about-pseudo-locales"></a>Recuperar informações sobre pseudo-locais

Você pode usar [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) para recuperar informações sobre uma pseudo-localidade. Passe para a função o nome da pseudo-localidade específica (consulte a lista de nomes acima). Por exemplo, "qps-plocm" para a pseudo-localidade espelhada.

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a>Usar LocaleNameToLCID com pseudo-localidades

Você pode chamar a função de mapeamento NLS [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) com o nome de uma pseudo-localidade.

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a>Habilitar pseudo-locais para enumeração

Em seu aplicativo, você pode chamar [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) para enumerar as localidades que o sistema reconhece. A parte das opções regionais e de idioma do painel de controle também chama **EnumSystemLocalesEx** para criar a lista de localidades que ele exibe. No entanto, por padrão, as quatro pseudo localidades listadas acima não são reconhecidas pelo sistema, portanto, não serão retornadas por **EnumSystemLocalesEx**. para sistemas do Windows Vista até e incluindo Windows 10, versão 1709, a solução é habilitar pseudo localidades adicionando chaves ao registro de Windows.

As edições são feitas sob a chave do \_ \_ controle do \\ sistema local \\ CurrentControlSet \\ Control \\ NLS para os idiomas instalados no sistema operacional. Você pode fazer essas configurações para habilitar as pseudo-localidades. Cada chave mostrada abaixo é o LCID hexadecimal correspondente à pseudo-localidade que está sendo habilitada. Cada valor é do tipo cadeia de caracteres (REG \_ SZ).

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

por Windows 10, a versão 1803, a edição do registro de Windows como esse não tem nenhum efeito. Mas você ainda pode chamar as APIs NLS sem enumeração com os nomes das pseudovariáveis (consulte os exemplos de código acima) para preencher a interface do usuário.

## <a name="related-topics"></a>Tópicos relacionados

* [Usando o suporte ao idioma nacional](using-national-language-support.md)
* [Pseudo-locais](pseudo-locales.md)
* [EnumSystemLocalesEx](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [GetLocaleInfoEx](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [LocaleNameToLCID](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
