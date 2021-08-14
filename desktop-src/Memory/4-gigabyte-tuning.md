---
description: 'Ajuste de 4 gigabyte: BCDEdit e Boot.ini'
ms.assetid: 991eb86f-9e6f-4084-8b6f-f979e42104b5
title: 'Ajuste de 4 gigabyte: BCDEdit e Boot.ini'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c8cd7b824669abbe684af91d848f445fe287c333c04abc08c676f3e125d2b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386673"
---
# <a name="4-gigabyte-tuning-bcdedit-and-bootini"></a>Ajuste de 4 gigabyte: BCDEdit e Boot.ini

Em edições de 32 bits do Windows, os aplicativos têm 4 GB (gigabyte) de espaço de endereço virtual disponível. O espaço de endereço virtual é dividido para que 2 GB estão disponíveis para o aplicativo e os outros 2 GB estão disponíveis apenas para o sistema. O recurso ajuste de 4 gigabyte (Ajuste de 4GT ou 4GT de RAM), habilitado com o comando *BCDEdit /set increaseuserva,* aumenta o espaço de endereço virtual disponível para o aplicativo em até 3 GB e reduz o valor disponível para o sistema entre 1 e 2 GB.

Para aplicativos com uso intensivo de memória, como DBMS (sistemas de gerenciamento de banco de dados), o uso de um espaço de endereço virtual maior pode fornecer benefícios consideráveis de desempenho e escalabilidade. No entanto, o cache de arquivos, o pool pa páginado e o pool não papagado são menores, o que pode afetar negativamente os aplicativos com E/S ou rede pesada. Portanto, talvez você queira testar seu aplicativo sob carga e examinar os contadores de desempenho para determinar se o aplicativo se beneficia do espaço de endereço maior.

Para habilitar o 4GT, use o [comando BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) para definir a opção de entrada de inicialização **increaseuserva** como um valor entre 2048 (2 GB) e 3072 (3 GB).

**Windows Server 2003 e anterior:** Para habilitar o 4GT, adicione a opção **/3GB** ao arquivo Boot.ini. Há suporte para a opção **/3GB** nos seguintes sistemas:

-   Windows Server 2003
-   Windows XP Professional

A **opção /3GB** disponibiliza um espaço completo de endereço virtual de 3 GB para aplicativos e reduz a quantidade disponível para o sistema para 1 GB. No Windows Server 2003, a quantidade de espaço de endereço disponível para aplicativos pode ser ajustada definindo a opção **/USERVA** no Boot.ini como um valor entre 2048 e 3072, o que aumenta a quantidade de espaço de endereço disponível para o sistema. Isso pode ajudar a manter o desempenho geral do sistema quando o aplicativo requer mais de 2 GB, mas menos de 3 GB de espaço de endereço.

Para permitir que um aplicativo use o espaço de endereço maior, de definido o sinalizador [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) no header da imagem. O linker incluído com Microsoft Visual C++ dá suporte à **opção /LARGEADDRESSAWARE** para definir esse sinalizador. Definir esse sinalizador e, em seguida, executar o aplicativo em um sistema que não tem suporte a 4GT não deve afetar o aplicativo.

Em edições de 64 bits do Windows, aplicativos de 32 bits marcados com o sinalizador [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) têm 4 GB de espaço de endereço disponível.

**Edições do Itanium Windows Server 2003:** Antes do SP1, os processos de 32 bits têm apenas 2 GB de espaço de endereço disponível.

Use as seguintes diretrizes para dar suporte a 4GT em aplicativos:

-   Endereços próximos ao limite de 2 GB normalmente são usados por várias DLLs do sistema. Portanto, um processo de 32 bits não pode alocar mais de 2 GB de memória contígua, mesmo se todo o espaço de endereço de 4 GB estiver disponível.
-   Para recuperar a quantidade total de espaço virtual do usuário, use a [**função GlobalMemoryStatusEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) Para recuperar o endereço de usuário mais alto possível, use a [**função GetSystemInfo.**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) Sempre detecte o valor real em runtime e evite usar definições de constante com fio rígido, como: `#define HIGHEST_USER_ADDRESS 0xC0000000` .
-   Evite comparações assinadas com ponteiros, pois eles podem fazer com que os aplicativos falham em um sistema habilitado para 4GT. Uma condição como a seguinte é falsa para um ponteiro acima de 2 GB: `if (pointer > 40000000)` .
-   O código que usa o bit mais alto de um ponteiro para uma finalidade definida pelo aplicativo falhará quando 4GT estiver habilitado. Por exemplo, uma palavra de 32 bits pode ser considerada um endereço de modo de usuário se estiver abaixo 0x80000000 e um código de erro, se acima. Isso não é verdadeiro com 4GT.

[**VirtualAlloc geralmente**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) retorna endereços baixos antes de endereços altos. Portanto, seu processo pode não usar endereços muito altos, a menos que ele aloce muita memória ou tenha um espaço de endereço virtual fragmentado. Para forçar alocações a alocar de endereços mais altos antes de endereços inferiores para fins de teste, especifique **MEM \_ TOP \_ DOWN** ao chamar **VirtualAlloc** ou de definir o seguinte valor do Registro como 0x100000:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** Session Manager Memory \\  \\ **Management** \\ **AllocationPreference**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Limites de memória para Windows versões](memory-limits-for-windows-releases.md)
</dt> <dt>

[Extensão de endereço físico](physical-address-extension.md)
</dt> <dt>

[Referência técnica 4GT](/previous-versions/windows/it-pro/windows-server-2003/cc778496(v=ws.10))
</dt> </dl>

 

 
