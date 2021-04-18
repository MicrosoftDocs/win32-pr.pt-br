---
title: Formatos da área de transferência
description: Uma janela pode posicionar mais de um objeto na área de transferência, cada um representando as mesmas informações em um formato de área de transferência diferente. Os usuários não precisam estar cientes dos formatos de área de transferência usados para um objeto na área de transferência.
ms.assetid: fe42baec-6b00-4816-b379-7f335da8a197
keywords:
- área de transferência, formatos
- área de transferência, Windows
- área de transferência, formatos padrão
- área de transferência, formatos registrados
- área de transferência, formatos sintetizados
- formatos de área de transferência padrão
- formatos de área de transferência registrados
- formatos de área de transferência sintetizados
- formatos de área de transferência em nuvem
- formatos de histórico da área de transferência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193ee4cc10c17846d974e50b17a464207026280b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105765015"
---
# <a name="clipboard-formats"></a>Formatos da área de transferência

Uma janela pode posicionar mais de um objeto na área de transferência, cada um representando as mesmas informações em um formato de área de transferência diferente. Os usuários não precisam estar cientes dos formatos de área de transferência usados para um objeto na área de transferência.

Os tópicos a seguir descrevem os formatos da área de transferência.

-   [Formatos de área de transferência padrão](#standard-clipboard-formats)
-   [Formatos de área de transferência registrados](#registered-clipboard-formats)
-   [Formatos de área de transferência privada](#private-clipboard-formats)
-   [Vários formatos de área de transferência](#multiple-clipboard-formats)
-   [Formatos de área de transferência sintetizados](#synthesized-clipboard-formats)
-   [Formatos de histórico de área de transferência da nuvem e área transferência](#cloud-clipboard-and-clipboard-history-formats)

## <a name="standard-clipboard-formats"></a>Formatos de área de transferência padrão

Os formatos de área de transferência definidos pelo sistema são chamados de *formatos de área de transferência padrão*. Esses formatos de área de transferência são descritos em [**formatos padrão da área de transferência**](standard-clipboard-formats.md).

## <a name="registered-clipboard-formats"></a>Formatos de área de transferência registrados

Muitos aplicativos funcionam com dados que não podem ser convertidos em um formato de área de transferência padrão sem perda de informações. Esses aplicativos podem criar seus próprios formatos de área de transferência. Um formato de área de transferência definido por um aplicativo é chamado de [formato de área de transferência registrado](#registered-clipboard-formats). Por exemplo, se um aplicativo de processamento de texto copiou texto formatado para a área de transferência usando um formato de texto padrão, as informações de formatação seriam perdidas. A solução seria registrar um novo formato de área de transferência, como RTF (Rich Text Format).

Para registrar um novo formato de área de transferência, use a função [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) . Essa função usa o nome do formato e retorna um valor inteiro sem sinal que representa o formato de área de transferência registrado. Para recuperar o nome do formato de área de transferência registrado, passe o valor inteiro não assinado para a função [**GetClipboardFormatName**](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea) .

Se mais de um aplicativo registrar um formato de área de transferência com exatamente o mesmo nome, o formato da área de transferência será registrado apenas uma vez. Ambas as chamadas para a função [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) retornam o mesmo valor. Dessa forma, dois aplicativos diferentes podem compartilhar dados usando um formato de área de transferência registrado.

## <a name="private-clipboard-formats"></a>Formatos de área de transferência privada

Um aplicativo pode identificar um formato de área de transferência particular definindo um valor no intervalo de **\_ PRIVATEFIRST do CF** até o **CF \_ PRIVATELAST**. Um aplicativo pode usar um formato de área de transferência particular para um formato de dados definido pelo aplicativo que não precisa ser registrado no sistema.

Os identificadores de dados associados a formatos de área de transferência privada não são liberados automaticamente pelo sistema. Se suas janelas usarem formatos de área de transferência privada, você poderá usar a mensagem [**\_ DESTROYCLIPBOARD do WM**](wm-destroyclipboard.md) para liberar todos os recursos relacionados que não são mais necessários.

Para obter mais informações sobre a mensagem do [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) , consulte [propriedade da área de transferência](clipboard-operations.md).

Um aplicativo pode posicionar identificadores de dados na área de transferência definindo um formato privado no intervalo de **CF \_ GDIOBJFIRST** por meio de **CF \_ GDIOBJLAST**. Ao usar valores nesse intervalo, o identificador de dados não é um identificador para um objeto Windows Graphics Device Interface (GDI), mas é um identificador alocado pela função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) com o sinalizador GMEMable \_ . Quando a área de transferência é esvaziada, o sistema exclui automaticamente o objeto usando a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .

## <a name="multiple-clipboard-formats"></a>Vários formatos de área de transferência

Uma janela pode posicionar mais de um objeto da área de transferência na área de transferência, cada um representando as mesmas informações em um formato de área de transferência diferente. Ao colocar informações na área de transferência, a janela deve fornecer dados em tantos formatos possíveis. Para descobrir quantos formatos são usados atualmente na área de transferência, chame a função [**CountClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats) .

Os formatos da área de transferência que contêm a maioria das informações devem ser colocados na área de transferência primeiro, seguidos por formatos menos descritivos. Uma janela colando informações da área de transferência normalmente recupera um objeto da área de transferência no primeiro formato que ele reconhece. Como os formatos da área de transferência são enumerados na ordem em que são colocados na área de transferência, o primeiro formato reconhecido também é o mais descritivo.

Por exemplo, suponha que um usuário Copie texto com estilo de um documento de processamento de texto. A janela que contém o documento pode primeiro inserir dados na área de transferência em um formato registrado, como RTF. Subsequentemente, a janela colocaria dados na área de transferência em um formato menos descritivo, como texto (**CF \_ Text**).

Quando o conteúdo da área de transferência é colado em outra janela, a janela recupera dados no formato mais descritivo que reconhece. Se a janela reconhecer RTF, os dados correspondentes serão colados no documento. Caso contrário, os dados de texto são colados no documento e as informações de formatação são perdidas.

## <a name="synthesized-clipboard-formats"></a>Formatos de área de transferência sintetizados

O sistema converte implicitamente os dados entre determinados formatos de área de transferência: se uma janela solicitar dados em um formato que não esteja na área de transferência, o sistema converterá um formato disponível para o formato solicitado. O sistema pode converter dados conforme indicado na tabela a seguir.



| Formato da área de transferência     | Formato de conversão    |
|----------------------|----------------------|
| **BITMAP do CF \_**       | **DIB do CF \_**          |
| **BITMAP do CF \_**       | **\_DIBV5 CF**        |
| **DIB do CF \_**          | **BITMAP do CF \_**       |
| **DIB do CF \_**          | **paleta do CF \_**      |
| **DIB do CF \_**          | **\_DIBV5 CF**        |
| **\_DIBV5 CF**        | **BITMAP do CF \_**       |
| **\_DIBV5 CF**        | **DIB do CF \_**          |
| **\_DIBV5 CF**        | **paleta do CF \_**      |
| **\_ENHMETAFILE CF**  | **\_METAFILEPICT CF** |
| **\_METAFILEPICT CF** | **\_ENHMETAFILE CF**  |
| **\_OEMTEXT CF**      | **texto do CF \_**         |
| **\_OEMTEXT CF**      | **\_UNICODETEXT CF**  |
| **texto do CF \_**         | **\_OEMTEXT CF**      |
| **texto do CF \_**         | **\_UNICODETEXT CF**  |
| **\_UNICODETEXT CF**  | **\_OEMTEXT CF**      |
| **\_UNICODETEXT CF**  | **texto do CF \_**         |



 

Se o sistema fornecer uma conversão automática de tipo para um formato de área de transferência específico, não haverá vantagem em colocar os formatos de conversão na área de transferência.

Se o sistema fornecer uma conversão automática de tipo para um formato de área de transferência específico e você chamar [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) para enumerar os formatos de dados da área de transferência, o sistema primeiro enumerará o formato que está na área de transferência, seguido pelos formatos para os quais ele pode ser convertido.

Ao copiar bitmaps, é melhor inserir o formato de **\_ DIBV5** do CF **ou do \_** CF na área de transferência. Isso ocorre porque as cores em um bitmap do CF (bitmap **dependente \_** de dispositivo) são relativas à paleta do sistema, que pode ser alterada antes de o bitmap ser colado. Se o formato de **\_ DIBV5** de **\_ DIB** ou CF do CF estiver na área de transferência e uma janela solicitar o formato de **\_ bitmap do CF** , o sistema renderizará o DIB (bitmap independente de dispositivo) usando a paleta atual nesse momento.

Se você colocar o formato de **\_ bitmap do CF** na área de transferência (e não o **CF \_ DIB**) **, o sistema \_** renderizará o formato de área de transferência do CF ou do **CF \_ DIBV5** assim que a área de transferência for fechada. Isso garante que a paleta correta seja usada para gerar o DIB. Se você posicionar o formato de **\_ DIBV5 do CF** com as informações de espaço de cores do bitmap na área de transferência, o sistema converterá os bits do bitmap do espaço de cores do bitmap para o espaço de cores sRGB quando o **CF \_ DIB** ou o **CF \_ DIBV5** for solicitado. Se o **CF \_ DIBV5** for solicitado quando não houver nenhuma informação de espaço de cores na área de transferência, o sistema retornará informações de espaço de cores sRGB na estrutura [**BITMAPV5HEADER**](/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header) . As conversões entre outros formatos de área de transferência ocorrem sob demanda.

Se a área de transferência contiver dados no formato de **\_ paleta do CF** , o aplicativo deverá usar as funções [**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette) e [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) para obter quaisquer outros dados na área de transferência em relação a essa paleta lógica.

Há dois formatos de área de transferência para metaarquivos: **CF \_ ENHMETAFILE** e **CF \_ METAFILEPICT**. Especifique **o \_ ENHMETAFILE CF** para os metaarquivos avançados e o **CF \_ METAFILEPICT** para metarquivos do Windows.

## <a name="cloud-clipboard-and-clipboard-history-formats"></a>Formatos de histórico de área de transferência da nuvem e área transferência

Algumas versões do Windows incluem a [área de transferência na nuvem](/windows/whats-new/whats-new-windows-10-version-1809#cloud-clipboard), que mantém um histórico dos itens de dados recentes da área de transferência e pode sincronizá-lo entre os dispositivos do usuário.
Se você não quiser que os dados que seu aplicativo coloca na área de transferência sejam incluídos no histórico da área de transferência ou sincronizados com outros dispositivos, seu aplicativo poderá controlar esse comportamento colocando dados em determinados [formatos de área de transferência registrados](#registered-clipboard-formats) cujos nomes são conhecidos pelo sistema Windows:

- **ExcludeClipboardContentFromMonitorProcessing** : Coloque os dados na área de transferência neste formato para impedir que todos os formatos da área de transferência sejam incluídos no histórico da área de transferência ou sincronizados com os outros dispositivos do usuário.
- **CanIncludeInClipboardHistory** : Coloque um valor **[DWORD](../WinProg/windows-data-types.md)** serializado de zero na área de transferência neste formato para impedir que todos os formatos da área de transferência sejam incluídos no histórico da área de transferência ou coloque um valor de um, para solicitar explicitamente que o item da área de transferência seja incluído no histórico da área de transferência. Isso não afeta a sincronização para outros dispositivos do usuário.
- **CanUploadToCloudClipboard** : Coloque um valor **[DWORD](../WinProg/windows-data-types.md)** serializado de zero na área de transferência neste formato para impedir que todos os formatos da área de transferência sejam sincronizados com os outros dispositivos do usuário, ou coloque um valor de um, para solicitar explicitamente que o item da área de transferência seja sincronizado com outros dispositivos. Isso não afeta o histórico da área de transferência do dispositivo local.

Assim como acontece com outros formatos de área de transferência registrados, você precisará usar a função [**RegisterClipboardFormat**](
/windows/win32/api/winuser/nf-winuser-registerclipboardformata) para obter um valor inteiro sem sinal que identifique cada um dos três formatos acima.