---
description: As funções auxiliares de API de versão são usadas para determinar a versão do sistema operacional em execução no momento. Para obter mais informações, consulte obtendo a versão do sistema.
ms.assetid: 1a70b1d9-ed66-4201-9921-4e26e4001020
title: Versão do Sistema Operacional
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: 73eb9a81880f29f9292713af46c5c79a7e9eb2de
ms.sourcegitcommit: 7ea69db68bca2b1592802e676ada8432a2583410
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/17/2020
ms.locfileid: "104008547"
---
# <a name="operating-system-version"></a>Versão do Sistema Operacional

As [funções auxiliares de API de versão](version-helper-apis.md) são usadas para determinar a versão do sistema operacional em execução no momento. Para obter mais informações, consulte [obtendo a versão do sistema](getting-the-system-version.md).

A tabela a seguir resume os números de versão mais recentes do sistema operacional.

| Sistema operacional | Número de versão |
|------------------|----------------|
| Windows 10       | 10,0\*         |
| Windows Server 2019 | 10,0\*      |
| Windows Server 2016 | 10,0\*      |
| Windows 8.1      | 6.3\*          |
| Windows Server 2012 R2 | 6.3\*    |
| Windows 8        | 6.2            |
| Windows Server 2012 | 6.2         |
| Windows 7        | 6.1            |
| Windows Server 2008 R2 | 6.1      |
| Windows Server 2008 | 6.0         |
| Windows Vista    | 6.0            |
| Windows Server 2003 R2 | 5.2      |
| Windows Server 2003 | 5.2         |
| Edição de 64 bits do Windows XP | 5.2   |
| Windows XP | 5.1                  |
| Windows 2000     | 5.0            |

**\*** Para aplicativos que foram manifestados para Windows 8.1 ou Windows 10. Aplicativos não manifestados para Windows 8.1 ou Windows 10 retornarão o valor de versão do sistema operacional Windows 8 (6,2). Para manifestar seus aplicativos para Windows 8.1 ou Windows 10, consulte [direcionando seu aplicativo para Windows](targeting-your-application-at-windows-8-1.md).<br/>

A identificação do sistema operacional atual geralmente não é a melhor maneira de determinar se um determinado recurso do sistema operacional está presente. Isso ocorre porque o sistema operacional pode ter novos recursos adicionados em uma DLL redistribuível. Em vez de usar as [funções auxiliares de API de versão](version-helper-apis.md) para determinar a plataforma do sistema operacional ou o número de versão, teste a presença do próprio recurso.

Para determinar a melhor maneira de testar um recurso, consulte a documentação do recurso de interesse. A lista a seguir aborda algumas técnicas comuns para detecção de recursos:

- Você pode testar a presença das funções associadas a um recurso. Para testar a presença de uma função em uma DLL do sistema, chame a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar a dll. Em seguida, chame a função [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para determinar se a função de interesse está presente na dll. Use o ponteiro retornado por **GetProcAddress** para chamar a função. Observe que, mesmo que a função esteja presente, pode ser um stub que simplesmente retorna um código de erro, como \_ chamada de erro \_ não \_ implementada.
- Você pode determinar a presença de alguns recursos usando a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Por exemplo, você pode detectar vários monitores de exibição chamando **GetSystemMetrics**(SM \_ CMONITORS).
- Há várias versões das DLLs redistribuíveis que implementam recursos de controle comum e de Shell. Para obter informações sobre como determinar quais versões estão presentes no sistema em que seu aplicativo está sendo executado, consulte o tópico [shell e versões de controles comuns](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)).

Se precisar de um sistema operacional específico, certifique-se de usá-lo como uma versão mínima com suporte, em vez de criar o teste para um sistema operacional. Dessa forma, o código de detecção continuará a funcionar em versões futuras do Windows.

Observe que um aplicativo de 32 bits pode detectar se ele está em execução no WOW64 chamando a função [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) . Ele pode obter informações adicionais do processador chamando a função [**GetNativeSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) .

Para obter mais informações, consulte [informações de versão do Windows 10](/windows/release-information/) e [folha de fatos do ciclo de vida do Windows](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).

