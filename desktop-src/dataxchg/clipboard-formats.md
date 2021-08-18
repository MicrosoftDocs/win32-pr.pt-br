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
ms.openlocfilehash: ac6bd2dc9dda8c8ccecd164123af68865005d9d28d328ce5489abf23926113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991336"
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

Um aplicativo pode posicionar identificadores de dados na área de transferência definindo um formato privado no intervalo de **CF \_ GDIOBJFIRST** por meio de **CF \_ GDIOBJLAST**. ao usar valores nesse intervalo, o identificador de dados não é um identificador para um objeto Windows Graphics Device Interface (GDI), mas é um identificador alocado pela função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) com o sinalizador GMEMable \_ . Quando a área de transferência é esvaziada, o sistema exclui automaticamente o objeto usando a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .

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

Ao copiar bitmaps, é melhor inserir o formato de **\_ DIBV5** do CF **ou do \_** CF na área de transferência. Isso porque as cores em um bitmap dependente do dispositivo (**CF \_ BITMAP**) são relativas à paleta do sistema, que pode mudar antes que o bitmap seja colar. Se o **formato \_ CF DIB** ou **CF \_ DIBV5** estiver na área de transferência e uma janela solicitar o formato **\_ BITMAP do CF,** o sistema renderizará o DIB (bitmap independente do dispositivo) usando a paleta atual no momento.

Se você colocar o formato **\_ BITMAP** do CF na área de transferência (e não no **CF \_ DIB),** o sistema renderizará o formato de área de transferência CF **\_ DIB** ou **CF \_ DIBV5** assim que a área de transferência for fechada. Isso garante que a paleta correta seja usada para gerar o DIB. Se você colocar o formato **\_ CF DIBV5** com as informações de espaço de cor de bitmap na área de transferência, o sistema converterá os bits de bitmap do espaço de cores do bitmap para o espaço de cores sRGB quando **CF \_ DIB** ou **CF \_ DIBV5** for solicitado. Se **CF \_ DIBV5** for solicitado quando não houver nenhuma informação de espaço de cor na área de transferência, o sistema retornará informações de espaço de cor sRGB na estrutura [**BITMAPV5HEADER.**](/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header) Conversões entre outros formatos de área de transferência ocorrem sob demanda.

Se a área de transferência contiver dados no formato **\_ PALETTE** cf, o aplicativo deverá usar as funções [**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette) e [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) para realizar quaisquer outros dados na área de transferência em relação a essa paleta lógica.

Há dois formatos de área de transferência para metarquivos: **CF \_ ENFILEAFILE** e **CF \_ METAFILEPICT.** **Especifique \_ CF EN LTDAFILE** para metadados aprimorados e **CF \_ METAFILEPICT** para Windows metadados.

## <a name="cloud-clipboard-and-clipboard-history-formats"></a>Formatos de histórico de área de transferência e área de transferência na nuvem

Algumas versões do [](/windows/whats-new/whats-new-windows-10-version-1809#cloud-clipboard)Windows incluem a Área de Transferência de Nuvem, que mantém um histórico de itens de dados recentes da área de transferência e pode sincroná-lo entre os dispositivos do usuário.
Se você não quiser que os dados que seu aplicativo coloca na área de transferência sejam incluídos no histórico da área de transferência ou sincronizados com outros dispositivos, seu aplicativo poderá controlar esse comportamento colocando dados em [determinados formatos](#registered-clipboard-formats) de área de transferência registrados cujos nomes são conhecidos pelo sistema Windows:

- **ExcludeClipboardContentFromMonitorProcessing:** coloque todos os dados na área de transferência nesse formato para impedir que todos os formatos da área de transferência estejam incluídos no histórico da área de transferência ou sincronizados com outros dispositivos do usuário.
- **CanIncludeInClipboardHistory:** coloque um valor **[DWORD](../WinProg/windows-data-types.md)** serializado de zero na área de transferência nesse formato para impedir que todos os formatos da área de transferência sejam incluídos no histórico da área de transferência ou coloque um valor de um em vez disso para solicitar explicitamente que o item da área de transferência seja incluído no histórico da área de transferência. Isso não afeta a sincronização com outros dispositivos do usuário.
- **CanUploadToCloudClipboard:** coloque um valor **[DWORD](../WinProg/windows-data-types.md)** serializado de zero na área de transferência nesse formato para impedir que todos os formatos da área de transferência sejam sincronizados com outros dispositivos do usuário ou coloque um valor de um para solicitar explicitamente que o item da área de transferência seja sincronizado com outros dispositivos. Isso não afeta o histórico da área de transferência do dispositivo local.

Assim como com outros formatos de área de transferência registrados, você precisará usar a função [**RegisterClipboardFormat**](
/windows/win32/api/winuser/nf-winuser-registerclipboardformata) para obter um valor inteiro sem sinal que identifica cada um dos três formatos acima.