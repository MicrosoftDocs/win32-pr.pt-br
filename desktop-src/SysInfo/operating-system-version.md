---
description: As funções auxiliares da API de versão são usadas para determinar a versão do sistema operacional em execução no momento. Para obter mais informações, consulte Obter a versão do sistema.
ms.assetid: 1a70b1d9-ed66-4201-9921-4e26e4001020
title: Versão do Sistema Operacional
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: ae90f4eac5546fccd7513d781234896fbbbda93ff3723a9ac1db438321ecf214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763948"
---
# <a name="operating-system-version"></a>Versão do Sistema Operacional

As [funções auxiliares da API de](version-helper-apis.md) versão são usadas para determinar a versão do sistema operacional em execução no momento. Para obter mais informações, consulte [Getting the System Version](getting-the-system-version.md).

A tabela a seguir resume os números de versão mais recentes do sistema operacional.

| Sistema operacional | Número de versão |
|------------------|----------------|
| Windows 10       | 10.0\*         |
| Windows Server 2019 | 10.0\*      |
| Windows Server 2016 | 10.0\*      |
| Windows 8.1      | 6.3\*          |
| Windows Server 2012 R2 | 6.3\*    |
| Windows 8        | 6.2            |
| Windows Server 2012 | 6.2         |
| Windows 7        | 6.1            |
| Windows Server 2008 R2 | 6.1      |
| Windows Server 2008 | 6,0         |
| Windows Vista    | 6,0            |
| Windows Server 2003 R2 | 5.2      |
| Windows Server 2003 | 5.2         |
| Windows XP 64-Bit Edition | 5.2   |
| Windows XP | 5.1                  |
| Windows 2000     | 5.0            |

**\*** Para aplicativos que foram manifestos para Windows 8.1 ou Windows 10. Aplicativos não manifestos para Windows 8.1 ou Windows 10 retornarão o valor Windows 8 versão do sistema operacional (6.2). Para manifesto de seus aplicativos para Windows 8.1 ou Windows 10, consulte [Direcionando seu aplicativo para](targeting-your-application-at-windows-8-1.md)Windows .<br/>

Identificar o sistema operacional atual geralmente não é a melhor maneira de determinar se um recurso de sistema operacional específico está presente. Isso porque o sistema operacional pode ter novos recursos adicionados em uma DLL redistribuível. Em vez de usar as funções auxiliares da [API](version-helper-apis.md) de versão para determinar a plataforma do sistema operacional ou o número de versão, teste a presença do próprio recurso.

Para determinar a melhor maneira de testar um recurso, consulte a documentação do recurso de interesse. A lista a seguir discute algumas técnicas comuns para detecção de recursos:

- Você pode testar a presença das funções associadas a um recurso. Para testar a presença de uma função em uma DLL do sistema, chame a [**função LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar a DLL. Em seguida, [**chame a função GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para determinar se a função de interesse está presente na DLL. Use o ponteiro retornado por **GetProcAddress** para chamar a função. Observe que, mesmo se a função estiver presente, pode ser um stub que apenas retorna um código de erro, como ERROR \_ CALL \_ NOT \_ IMPLEMENTED.
- Você pode determinar a presença de alguns recursos usando a [**função GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Por exemplo, você pode detectar vários monitores de exibição chamando **GetSystemMetrics**(SM \_ CMONITORS).
- Há várias versões das DLLs redistribuíveis que implementam recursos de shell e controle comuns. Para obter informações sobre como determinar quais versões estão presentes no sistema em que seu aplicativo está sendo executado, consulte o tópico [Shell e Versões de Controles Comuns](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)).

Se você precisar exigir um sistema operacional específico, certifique-se de usá-lo como uma versão mínima com suporte, em vez de projetar o teste para um sistema operacional. Dessa forma, seu código de detecção continuará a funcionar em versões futuras do Windows.

Observe que um aplicativo de 32 bits pode detectar se ele está em execução em WOW64 chamando a [**função IsWow64Process.**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) Ele pode obter informações adicionais do processador chamando a [**função GetNativeSystemInfo.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

Para obter mais informações, consulte [Windows 10 de versão e](/windows/release-information/) Windows de fatos do ciclo de [vida.](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)

