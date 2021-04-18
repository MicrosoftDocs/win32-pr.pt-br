---
title: Suporte a IDN no WinINet
description: A partir do Windows Server 2008 e do Windows Vista, a parte do host da URL Unicode é convertida para o IDN (nome de domínio internacionalizado).
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366577"
---
# <a name="idn-support-in-wininet"></a>Suporte a IDN no WinINet

A partir do Windows Server 2008 e do Windows Vista, a parte do host da URL Unicode é convertida para o IDN (nome de domínio internacionalizado). Partes separadas da codificação de URL Unicode também podem ser modificadas por configurações definidas pelo aplicativo. As versões ANSI da API do WinINet continuam a enviar a URL pela transmissão, conforme inserido pelo aplicativo, no entanto, as versões Unicode do WinINet da API agora estão em conformidade com o padrão IDN (RFC3490) para codificações de URL.

Por padrão, quando uma URL é inserida como um parâmetro Unicode, a parte do host, para conexões diretas e proxy, é convertida no formato IDN. O aplicativo tem a opção de desabilitar a formatação de host IDN definindo a opção **Internet \_ Option \_ IDN** . A conversão de host IDN pode ser habilitada somente nas conexões diretas ou de proxy usando os sinalizadores de **\_ \_ \_ proxy** de IDN **\_ \_ \_ direto** ou sinalizador da Internet com a **\_ opção \_ IDNs** da Internet.

O exemplo de código a seguir mostra como desabilitar a conversão de host IDN para o proxy e as conexões diretas.

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

Se a formatação do host IDN estiver desabilitada, o aplicativo terá a opção de especificar a página de código desejada usando a **\_ página de \_ código da opção da Internet**.

O exemplo de código a seguir mostra como especificar a página de código em Japonês.

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

A parte do caminho da URL é codificada por padrão, e os segmentos restantes da URL, a consulta ou o fragmento, são convertidos na página de código padrão do sistema (CP \_ ACP).

O exemplo a seguir mostra como especificar a página de código do idioma coreano para a parte do caminho da URL.

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

A tabela a seguir define as opções que dão suporte a IDN. Para obter mais informações, consulte o tópico [sinalizadores de opção](option-flags.md) .



| Opção                            | Descrição                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| página de código da \_ opção da Internet \_        | Essa opção é definida na solicitação, ou no identificador de conexão, para especificar um esquema de codificação de página de código para a parte do host da URL. Essa opção será ignorada se o IDN estiver habilitado.                                                      |
| \_caminho de \_ página de código de opção da Internet \_  | Essa opção é definida na solicitação, ou o identificador de conexão habilita o esquema de codificação especificado para a parte do caminho da URL. Por padrão, a parte do caminho da URL é codificada em UTF8.                                         |
| opção de página de código de INTERNET \_ \_ \_ extra | Definir essa opção na solicitação ou no identificador de conexão habilita o esquema de codificação especificado para a parte extra da URL. Por padrão, a parte extra da URL é codificada na página de código padrão do sistema (CP \_ ACP). |
| opção de INTERNET \_ \_ IDN             | Essa opção pode ser usada na solicitação ou no identificador de conexão para habilitar ou desabilitar a conversão do host IDN. Quando o IDN é desabilitado, o WinINet usa a página de código do sistema padrão para codificar a parte de host ou autoridade da URL.       |



 

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 