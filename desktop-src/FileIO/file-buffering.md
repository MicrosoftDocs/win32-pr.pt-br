---
description: Descreve as considerações sobre O controle de aplicativo do buffer de arquivo, também conhecido como e/s (entrada/saída) de arquivo sem buffer.
ms.assetid: ae1e5d0f-9b55-4aae-8402-b9c8e33d9363
title: Armazenar arquivo em buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44f6724622b2c3116fa24a6109efb6c0d9f1d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171502"
---
# <a name="file-buffering"></a>Armazenar arquivo em buffer

Este tópico aborda as várias considerações para o controle de aplicativo do buffer de arquivo, também conhecido como e/s (entrada/saída) de arquivo sem buffer. O buffer de arquivos geralmente é tratado pelo sistema nos bastidores e é considerado parte do [cache de arquivos](file-caching.md) no sistema operacional Windows, a menos que especificado de outra forma. Embora os termos *cache* e *buffer* , às vezes, sejam usados de maneira intercambiável, este tópico usa o termo *buffering* especificamente no contexto explicando como interagir com os dados que não estão sendo armazenados em cache (em buffer) pelo sistema, onde ele é, de outra forma, parte do controle direto de aplicativos de modo de usuário.

Ao abrir ou criar um arquivo com a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , o sinalizador de **arquivo sem sinalizador de \_ \_ \_ buffer** pode ser especificado para desabilitar o cache do sistema de dados que estão sendo lidos ou gravados no arquivo. Embora isso forneça controle completo e direto sobre O buffer de e/s de dados, no caso de arquivos e dispositivos semelhantes, há requisitos de alinhamento de dados que devem ser considerados.

> [!Note]  
> Essas informações de alinhamento se aplicam à e/s em dispositivos, como arquivos que dão suporte à busca e ao conceito de ponteiros de posição de arquivo (ou *deslocamentos*). Para dispositivos que não buscam, como pipes nomeados ou dispositivos de comunicação, desativar o buffer pode não exigir nenhum alinhamento específico. Quaisquer limitações ou eficiências que possam ser obtidas pelo alinhamento nesse caso dependem da tecnologia subjacente.

 

Em um exemplo simples, o aplicativo abriria um arquivo para acesso de gravação com o sinalizador **File \_ Flag \_ no \_ buffer** e, em seguida, executaria uma chamada para a função [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) usando um buffer de dados definido no aplicativo. Esse buffer local é, nessas circunstâncias, efetivamente o único buffer de arquivo que existe para essa operação. Devido ao layout do disco físico, ao layout do armazenamento do sistema de arquivos e ao controle da posição do ponteiro de arquivo no nível do sistema, essa operação de gravação falhará, a menos que os buffers de dados definidos localmente atendam a certos critérios de alinhamento, discutidos na seção a seguir.

> [!Note]  
> A discussão sobre Caching não considera nenhum cache de hardware no próprio disco físico, o que não é garantido que esteja dentro do controle direto do sistema em qualquer caso. Isso não tem nenhum efeito sobre os requisitos especificados neste tópico.

 

Para obter mais informações sobre como o **sinalizador de arquivo \_ \_ sem \_ buffer** interage com outros sinalizadores relacionados ao cache, consulte [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

## <a name="alignment-and-file-access-requirements"></a>Requisitos de acesso de alinhamento e arquivo

Conforme discutido anteriormente, um aplicativo deve atender a certos requisitos ao trabalhar com arquivos abertos com o **sinalizador de arquivo \_ \_ sem \_ buffer**. As seguintes especificações se aplicam:

-   Tamanhos de acesso de arquivo, incluindo o deslocamento de arquivo opcional na estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , se especificado, devem ser para um número de bytes que é um inteiro múltiplo do tamanho do setor de volume. Por exemplo, se o tamanho do setor for 512 bytes, um aplicativo poderá solicitar leituras e gravações de 512, 1.024, 1.536 ou 2.048 bytes, mas não de 335, 981 ou 7.171 bytes.
-   Os endereços de buffer de acesso a arquivos para operações de leitura e gravação devem ser alinhados ao setor físico, o que significa que alinhado em endereços na memória que são múltiplos inteiros do tamanho do setor físico do volume. Dependendo do disco, esse requisito pode não ser imposto.

Os desenvolvedores de aplicativos devem anotar os novos tipos de dispositivos de armazenamento introduzidos no mercado com um tamanho de setor de mídia física de 4.096 bytes. O nome do setor para esses dispositivos é "Advanced Format". Como pode haver problemas de compatibilidade com a introdução direta de 4.096 bytes como a unidade de endereçamento para a mídia, uma solução de compatibilidade temporária é introduzir dispositivos que emulam um dispositivo de armazenamento de setor de 512 bytes regular, mas disponibilizam informações sobre o tamanho de setor real por meio de comandos ATA e SCSI padrão.

Como resultado dessa emulação, há, na essência, dois tamanhos de setor que os desenvolvedores precisarão entender:

-   Setor lógico: a unidade usada para endereçamento de bloco lógico para a mídia. Também podemos considerar isso como a menor unidade de gravação que o armazenamento pode aceitar. Esta é a "emulação".
-   Setor físico: a unidade para a qual as operações de leitura e gravação para o dispositivo são concluídas em uma única operação. Essa é a unidade de gravação atômica e qual e/s sem buffer precisará ser alinhada para ter as características de desempenho e confiabilidade ideais.

A maioria das APIs do Windows atuais, como o disco do IOCTL [](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea), a [**\_ \_ \_ \_ geometria da unidade**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_geometry) e GetDiskFreeSpace, retornará o tamanho do setor lógico, mas o tamanho do setor físico pode ser recuperado por meio do código de controle da [**\_ \_ \_ propriedade de consulta de armazenamento do IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) , com as informações relevantes contidas no membro **BytesPerPhysicalSector** na estrutura do [**\_ \_ \_ descritor de alinhamento de acesso de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor) . Para obter um exemplo, consulte o código de exemplo no [**\_ \_ \_ descritor de alinhamento de acesso de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor). A Microsoft recomenda enfaticamente que os desenvolvedores alinhem e/s sem buffer ao tamanho do setor físico, conforme relatado pelo código de controle da propriedade de consulta de armazenamento do IOCTL para ajudar a garantir que seus aplicativos estejam preparados para essa transição de tamanho de setor. **\_ \_ \_**

**Windows Server 2003 e Windows XP:** A estrutura do [**\_ \_ \_ descritor de alinhamento de acesso de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor) não está disponível. Ele foi introduzido com o Windows Vista e o Windows Server 2008.

Como os endereços de buffer para operações de leitura e gravação devem ser alinhados ao setor, o aplicativo deve ter controle direto de como esses buffers são alocados. Uma maneira de alinhar os buffers do setor é usar a função do [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) para alocar os buffers. Considere o seguinte:

-   O [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) aloca a memória que está alinhada em endereços que são múltiplos inteiros do tamanho de página do sistema. O tamanho da página é 4.096 bytes em x64 e x86 ou 8.192 bytes para sistemas baseados em Itanium. Para obter mais informações, consulte a função [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .
-   O tamanho do setor geralmente é de 512 a 4.096 bytes para dispositivos de armazenamento de acesso direto (discos rígidos) e 2.048 bytes para CD-ROMs.
-   Os tamanhos de página e de setor são potências de 2.

Portanto, na maioria das situações, a memória alinhada por página também será alinhada ao setor, pois o caso em que o tamanho do setor é maior do que o tamanho da página é raro.

Outra maneira de obter buffers de memória alinhados manualmente é usar a função [ \_ \_ malloc alinhada](/cpp/c-runtime-library/reference/aligned-malloc?view=vs-2019) da biblioteca do C Run-Time. Para obter um exemplo de como controlar manualmente o alinhamento do buffer, consulte o exemplo de código de linguagem C++ na seção de código de exemplo de [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile).

 

 
