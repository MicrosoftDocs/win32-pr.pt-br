---
description: Uma hora do arquivo é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos decorridos desde as 12:00 A.M. 1º de janeiro de 1601 UTC (tempo Universal Coordenado). O sistema registra os horários dos arquivos quando os aplicativos criam, acessam e gravam em arquivos.
ms.assetid: 52d80b82-9ab0-4631-9e70-85df21da4946
title: Horas de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1492597b4e71775974ed8b19f6109c5900a8a28720b769c1c10dcf2f70166b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764487"
---
# <a name="file-times"></a>Horas de arquivo

Uma *hora do arquivo* é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos decorridos desde as 12:00 A.M. 1º de janeiro de 1601 UTC (tempo Universal Coordenado). O sistema registra os horários dos arquivos quando os aplicativos criam, acessam e gravam em arquivos.

O sistema de arquivos NTFS armazena valores de tempo no formato UTC, portanto, eles não são afetados por alterações no fuso horário ou no horário de verão. O sistema de arquivos FAT armazena valores de tempo com base na hora local do computador. Por exemplo, um arquivo que é salvo em 3:13h PST em Washington é visto como 6:13h EST em Nova York em um volume NTFS, mas é visto como 3:13h EST em Nova York em um volume FAT.

Os carimbos de data/hora são atualizados em vários momentos e por vários motivos. A única garantia de um carimbo de data/hora do arquivo é que a hora do arquivo é refletida corretamente quando o identificador que faz a alteração é fechado.

Nem todos os sistemas de arquivos podem registrar a criação e os últimos tempos de acesso, e nem todos os sistemas de arquivos os registram da mesma maneira. Por exemplo, a resolução de tempo de criação em FAT é de 10 milissegundos, enquanto o tempo de gravação tem uma resolução de 2 segundos e o tempo de acesso tem uma resolução de 1 dia, portanto, é realmente a data de acesso. O sistema de arquivos NTFS atrasa as atualizações para o último horário de acesso de um arquivo em até 1 hora após o último acesso.

Para recuperar os tempos de arquivo para um arquivo especificado, use a função [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) . **GetFileTime** copia a criação, o último acesso e as últimas horas de gravação para estruturas [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) individuais. Você também pode recuperar os horários de arquivo usando as funções [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) . Essas funções copiam as horas do arquivo para estruturas **FILETIME** em uma estrutura de [**dados de \_ localização \_ do Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) . Ao gravar em um arquivo, a hora da última gravação não é totalmente atualizada até que todos os identificadores usados para gravação sejam fechados.

Para definir os tempos de arquivo para um arquivo, use a função [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) . Essa função permite que você modifique as horas de criação, último acesso e última gravação sem alterar o conteúdo do arquivo. Você pode comparar os tempos de arquivos diferentes usando a função [**CompareFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime) . A função compara duas horas de arquivo e retorna um valor que indica qual é a hora posterior ou retorna 0 (zero) se as horas forem iguais.

Se você planeja modificar os horários de arquivo para arquivos especificados, você pode converter uma data e hora do dia em uma hora de arquivo usando a função [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) . Você também pode obter a hora do sistema em uma estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) chamando a função [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) .

Para facilitar a exibição de uma hora do arquivo para um usuário, use a função [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) . **FileTimeToSystemTime** converte a hora do arquivo e copia o mês, o dia, o ano e a hora do dia a partir da hora do arquivo para uma estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .

## <a name="file-times-and-daylight-saving-time"></a>Horas de arquivo e horário de verão

Você deve tomar cuidado ao usar os horários de arquivo se o usuário tiver definido o sistema para se ajustar automaticamente para o horário de verão.

Para converter uma hora de arquivo em hora local, use a função [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) . No entanto, o **FileTimeToLocalFileTime** usa as configurações atuais para o fuso horário e o horário de verão. Portanto, se for o horário de verão, ele levará o horário de verão em conta, mesmo se a hora do arquivo que você está convertendo estiver no horário padrão.

O sistema de arquivos FAT registra as horas no disco na hora local. [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) recupera horas UTC em cache do sistema de arquivos FAT. Quando se torna o horário de verão, o tempo recuperado por **GetFileTime** é de uma hora, pois o cache não é atualizado. Quando você reinicia o computador, o tempo em cache que o **GetFileTime** recupera está correto. [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) recupera a hora local do sistema de arquivos FAT e a converte em UTC usando as configurações atuais para o fuso horário e o horário de verão. Portanto, se for o horário de verão, o **FindFirstFile** usará o horário de verão, mesmo se a hora do arquivo que você está convertendo estiver no horário padrão.

O sistema de arquivos NTFS registra os horários em disco em UTC. Para considerar o horário de verão ao converter uma hora de arquivo em uma hora local, use a seguinte sequência de funções em vez de usar [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime):

-   [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)
-   [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)
-   [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)

## <a name="file-times-and-cdfs"></a>Horas de arquivo e CDFS

Os carimbos de data e hora dos arquivos que estão localizados ou originários da mídia usando o sistema de arquivos do CD (CDFS) são ajustados para o fuso horário local. O ISO 9660 afirma que o CDFS é exibir as informações de data corretamente para o fuso horário local. Isso é feito para que as datas de arquivos em CDFS sejam exibidas da mesma forma que no formato de disco universal (UDF). UDF é o padrão mais recente para mídia de distribuição. Se seu código depende das informações de data não modificadas de um arquivo que reside ou se origina da mídia usando CDFS, ele pode não funcionar corretamente.

 

 
