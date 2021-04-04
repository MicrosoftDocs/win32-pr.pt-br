---
description: Os nomes DNS consistem em um ou mais componentes separados por um ponto (por exemplo, msdn.microsoft.com).
ms.assetid: 7e083cb5-cf0a-4284-8b54-dac856910c44
title: Nomes do computador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf076f42e3353aa03db951e9dec428766cf4895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837493"
---
# <a name="computer-names"></a>Nomes do computador

Os nomes DNS consistem em um ou mais componentes separados por um ponto (por exemplo, msdn.microsoft.com). Cada componente pode ter até 63 bytes. Cada nome pode ter até 255 bytes no total. Os nomes DNS são representados no conjunto de caracteres UTF-8 ou Unicode. O nome não diferencia maiúsculas de minúsculas. Para obter mais informações, consulte [**DnsValidateName**](/windows/desktop/api/windns/nf-windns-dnsvalidatename).

Um computador é identificado exclusivamente pelo nome DNS totalmente qualificado, que consiste em seu nome de host DNS e o nome do domínio DNS ao qual ele está atribuído. Para recuperar o nome DNS totalmente qualificado de um computador, nome de host DNS ou nome de domínio DNS, chame a função [**GetComputerNameEx devia**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) . Para definir o nome de host DNS de um computador ou o nome de domínio DNS, chame a função [**SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) . As alterações de nome não entram em vigor até que o usuário reinicie o computador.

Os nomes NetBIOS consistem em até 15 bytes de caracteres OEM, incluindo letras, dígitos, hifens e pontos. Alguns caracteres são específicos do conjunto de caracteres. Normalmente, os nomes NetBIOS são representados no conjunto de caracteres OEM. O conjunto de caracteres OEM depende da localidade. Alguns conjuntos de caracteres OEM representam determinados caracteres como dois bytes. Os nomes NetBIOS, por convenção, são representados em letras maiúsculas onde o algoritmo de conversão de minúsculas para maiúsculas é dependente do conjunto de caracteres OEM.

As funções [**SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) e [**GetComputerNameEx devia**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) também podem definir e recuperar o nome NetBIOS do computador. Por convenção, o nome NetBIOS e o nome do host DNS são interdependentes. Quando você modifica o nome DNS, o nome NetBIOS também é atualizado. O nome NetBIOS é a representação OEM do nome de host DNS até o máximo de \_ caracteres de comprimento de ComputerName \_ . Se você definir um nome de host DNS com mais do que o máximo de \_ caracteres de comprimento de ComputerName \_ , o nome NetBIOS será definido como uma versão truncada do nome de host DNS. Caso contrário, o nome do host DNS inteiro será convertido no nome NetBIOS do OEM. Aviso: se você modificar o nome NetBIOS para que ele não seja um mapeamento truncado do nome DNS, você interromperá os aplicativos que usam funções como [**DnsHostnameToComputerName**](/windows/desktop/api/Winbase/nf-winbase-dnshostnametocomputernamea) que dependem dessa Convenção.

 

 
