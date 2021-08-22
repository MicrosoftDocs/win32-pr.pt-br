---
description: Os nomes DNS consistem em um ou mais componentes separados por um ponto (por exemplo, msdn.microsoft.com).
ms.assetid: 7e083cb5-cf0a-4284-8b54-dac856910c44
title: Nomes do computador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8687d6d510247a2bbb2850e6a668a63f0108b2bc344ed161cb73e28d2b47eeaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885786"
---
# <a name="computer-names"></a>Nomes do computador

Os nomes DNS consistem em um ou mais componentes separados por um ponto (por exemplo, msdn.microsoft.com). Cada componente pode ter até 63 bytes. Cada nome pode ter até 255 bytes no total. Os nomes DNS são representados no conjunto de caracteres UTF-8 ou Unicode. O nome não é sensível a minúsculas. Para obter mais informações, [**consulte DnsValidateName**](/windows/desktop/api/windns/nf-windns-dnsvalidatename).

Um computador é identificado exclusivamente por seu nome DNS totalmente qualificado, que consiste no nome do host DNS e no nome do domínio DNS ao qual ele é atribuído. Para recuperar o nome DNS totalmente qualificado de um computador, o nome do host DNS ou o nome de domínio DNS, chame a [**função GetComputerNameEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) Para definir o nome do host DNS de um computador ou o nome de domínio DNS, chame a [**função SetComputerNameEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) As alterações de nome não entre em vigor até que o usuário reinicie o computador.

Os nomes NetBIOS consistem em até 15 bytes de caracteres OEM, incluindo letras, dígitos, hifens e pontos. Alguns caracteres são específicos para o conjunto de caracteres. Os nomes NetBIOS normalmente são representados no conjunto de caracteres OEM. O conjunto de caracteres OEM depende da localidade. Alguns conjuntos de caracteres OEM representam determinados caracteres como dois bytes. Os nomes NetBIOS, por convenção, são representados em letras maiúsculas, em que o algoritmo de conversão de minúsculas para maiúsculas depende do conjunto de caracteres OEM.

As [**funções SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) e [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) também podem definir e recuperar o nome NetBIOS do computador. Por convenção, o nome NetBIOS e o nome do host DNS são interdependentes. Quando você modifica o nome DNS, o nome NetBIOS também é atualizado. O nome NetBIOS é a representação OEM do nome do host DNS até os \_ caracteres MAX COMPUTERNAME \_ LENGTH. Se você definir um nome de host DNS com mais de caracteres MAX COMPUTERNAME LENGTH, o nome NetBIOS será definido como uma versão truncada do nome \_ \_ do host DNS. Caso contrário, todo o nome do host DNS será convertido no nome OEM NetBIOS. Aviso: se você modificar o nome NetBIOS para que ele não seja um mapeamento truncado do nome DNS, você quebrará aplicativos que usam funções como [**DnsHostnameToComputerName**](/windows/desktop/api/Winbase/nf-winbase-dnshostnametocomputernamea) que dependem dessa convenção.

 

 
