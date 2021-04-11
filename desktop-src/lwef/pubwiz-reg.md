---
title: Registrando um serviço
description: Para adicionar seu serviço à lista de provedores no assistente de publicação na Web ou no assistente de ordenação de impressão online, você deve adicionar a chave apropriada e seus valores ao registro do Windows.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- registrar, serviços
- Assistente de publicação na Web, registrando
- Assistente de ordenação de impressão online, registrando
- registrar, assistente de publicação na Web
- registrar, assistente de ordenação de impressão online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497133d7f0a769fce987745a2341a2e501fe7a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104172895"
---
# <a name="registering-a-service"></a>Registrando um serviço

Para adicionar seu serviço à lista de provedores no assistente de publicação na Web ou no assistente de ordenação de impressão online, você deve adicionar a chave apropriada e seus valores ao registro do Windows.

## <a name="required-keys-and-values"></a>Chaves e valores necessários

Para adicionar seu serviço à lista de provedores para o assistente de publicação na Web, adicione uma chave, conforme mostrado abaixo.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Para adicionar seu serviço à lista de provedores para o assistente de ordenação de impressão online, adicione uma chave, conforme mostrado abaixo.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Cada um dos valores é uma cadeia de caracteres do tipo REG \_ sz. Forneça seus dados, conforme explicado na tabela a seguir. 

| Nome do valor     | Explicação                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IconPath       | O caminho completo para o arquivo de ícone, incluindo o nome do arquivo.                                                                                                                                                                                                                                                                                                                                                                        |
| DisplayName    | O nome exibido para o serviço na lista de provedores do assistente.                                                                                                                                                                                                                                                                                                                                                             |
| Descrição    | Uma breve descrição do seu serviço. Essa descrição também é exibida na lista de provedores do assistente diretamente abaixo do nome do seu serviço.                                                                                                                                                                                                                                                                                    |
| HREF           | A URL da primeira página do serviço.                                                                                                                                                                                                                                                                                                                                                                                      |
| SupportedTypes | Os tipos de arquivo com suporte no seu serviço. Por exemplo, *\* . jpg*. Ao especificar apenas determinados tipos de arquivo, seu serviço só aparece quando esses tipos de arquivo foram selecionados. Se mais de um tipo de arquivo tiver sido selecionado, seu serviço será exibido se qualquer um desses tipos de arquivo tiver suporte do seu serviço. Se você quiser especificar vários tipos de arquivo, separe-os na lista com pontos-e-vírgulas. Por exemplo, *\* . jpg; \* . BMP*. |



 

Veja a seguir um exemplo completo de um serviço de processamento de fotos intitulado "myfornecedor".

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

Quando a URL do serviço é chamada, dois valores são adicionados ao final da URL – LCID e LangID. Por exemplo, a cadeia de caracteres de URL para o exemplo acima pode ser https: \/ /www.MyProvider.com/Intro.htm? lcid = 1033&LangID = 1033. Essas variáveis são usadas para informações de idioma e localização.

-   **LCID** é usado para informar o servidor do país/região do cliente e as configurações de idioma. Ele não é usado para determinar o idioma da interface do usuário do cliente, mas é usado para determinar o formato adequado para moeda, data e hora e outros dados específicos da região.
-   o **LangID** é usado para informar o servidor da configuração de idioma padrão do cliente para que ele possa usar o idioma apropriado na interface do usuário.

 

 




