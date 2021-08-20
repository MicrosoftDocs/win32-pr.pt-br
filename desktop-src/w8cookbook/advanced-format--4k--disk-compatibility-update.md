---
title: Atualização de compatibilidade de disco de formato avançado (4K)
description: Atualização de compatibilidade de disco de formato avançado (4K)
ms.assetid: 2C9EB0CF-D27B-457A-8FE6-24824BCC084C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cf89345dfc33826c4eb1f155083793726de7d70bc95c1dcdda96644d5d1173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117672186"
---
# <a name="advanced-format-4k-disk-compatibility-update"></a>Atualização de compatibilidade de disco de formato avançado (4K)

## <a name="platforms"></a>Plataformas

**clientes** Windows XP, Windows Vista, Windows 7, Windows 7 SP1, Windows 8     
**servidores** Windows server 2003, Windows server 2008, Windows server 2008 r2, Windows Server 2008 R2 SP1, Windows Server 2012, Windows Server 2012 r2 Windows Server 2016     


## <a name="description"></a>Descrição

este artigo é uma versão atualizada do artigo intitulada atualização de compatibilidade de disco do 512e (emulação de 512 bytes), que foi lançada para o Windows 7 sp1 e o Windows Server 2008 R2 SP1. esta atualização contém muitas informações novas, algumas das quais são aplicáveis somente a Windows 8 e Windows Server 2012.

As densidades areais estão cada vez mais anuais e com o advento recente de 3 TB de discos, os mecanismos de correção de erros usados para lidar com a proporção de sinal-para-ruído (SNR) de redução estão ficando ineficientes; ou seja, uma maior quantidade de sobrecarga é necessária para garantir que a mídia seja utilizável. Uma das soluções do setor de armazenamento para melhorar esse mecanismo de correção de erros é introduzir um formato de mídia físico diferente que inclua um tamanho de setor físico maior. Esse novo formato de mídia física é chamado de formato avançado. Portanto, não é mais seguro fazer suposições sobre o tamanho do setor de dispositivos de armazenamento modernos, e os desenvolvedores precisarão estudar as suposições subjacentes a seu código para determinar se há um impacto.

este tópico apresenta o efeito de dispositivos de armazenamento de formato avançado em software, discute o que os aplicativos podem fazer para ajudar a dar suporte a esse tipo de mídia e discute a infraestrutura que a Microsoft introduziu com o Windows Vista, Windows 7 e Windows 8 para permitir que os desenvolvedores ofereçam suporte a esses tipos de dispositivos. embora o material apresentado neste tópico forneça diretrizes para melhorar a compatibilidade com discos de formato avançado, as informações se aplicam em geral a todos os sistemas com discos de formato avançado que executam o Windows Vista, Windows 7 e Windows 8.

**Resumo dos novos recursos relacionados ao setor de grande porte**

a lista abaixo resume os novos recursos fornecidos como parte do Windows 8 e Windows Server 2012 para ajudar a melhorar a experiência do cliente e do desenvolvedor com discos de setor grande. Uma descrição mais detalhada para cada item é seguida.

-   baseia-se no suporte a Windows 7 SP1 para 4k disks with emulation (512e) e fornece suporte completo à caixa de entrada para discos com tamanho de setor de 4k sem emulação (nativo de 4k). Alguns aplicativos e cenários com suporte incluem:
    -   capacidade de instalar o Windows e inicializar a partir de um disco de setor de 4k sem emulação (disco nativo de 4k)
    -   VHD e novo formato de arquivo VHDX
    -   Suporte completo para HyperV
    -   Windows backup
    -   Suporte completo no sistema de arquivos NT (NTFS)
    -   suporte completo com novos Espaços de Armazenamento e pools (SSP)
    -   Suporte completo com o Windows Defender
-   Fornece uma nova API para consultar o tamanho do setor físico (FileFsSectorSizeInformation):
    -   Disponível para volumes de rede
    -   Pode ser emitido para qualquer identificador de arquivo
    -   Disponível para aplicativos sem privilégios
    -   Modelo de uso mais amigável
-   inclui o utilitário de linha de comando fsutil aprimorado para consultar o tamanho do setor lógico e físico do volume com informações de alinhamento (a versão básica do utilitário sem informações de alinhamento está disponível para o Windows 7 com microsoft kb 982018 e Windows Server 2008 R2 com microsoft kb 982018)

**Introdução aos discos de formato avançado (4K)**

Um dos problemas de introduzir essa alteração no formato de mídia é o potencial para introduzir problemas de compatibilidade com software e hardware existentes. Como solução de compatibilidade temporária, o setor de armazenamento está inicialmente introduzindo discos que emulam um disco de setor de 512 bytes comum, mas disponibilizam informações sobre o tamanho real do setor por meio de comandos ATA e SCSI padrão. Como resultado dessa emulação, há, em essência, dois tamanhos de setor:

**Setor lógico:** A unidade usada para endereçamento de bloco lógico para a mídia. Também podemos considerar isso como a menor unidade de gravação que o armazenamento pode aceitar. Esta é a emulação.   
**Setor físico:** A unidade para a qual as operações de leitura e gravação para o dispositivo são concluídas em uma única operação. Esta é a unidade de gravação atômica.  
 a maioria das APIs de Windows atuais, como \_ o disco de IOCTL \_ obter \_ \_ geometria de unidade retornará o tamanho do setor lógico, mas o tamanho do setor físico pode ser recuperado por meio do código de controle de propriedade de <a href="/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property">consulta de armazenamento do ioctl \_ \_ \_ </a> , com as informações relevantes contidas no campo BytesPerPhysicalSector na estrutura do <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor"> \_ \_ \_ descritor de alinhamento de acesso de armazenamento</a> . Isso é discutido em mais detalhes posteriormente neste artigo.

**Tipos iniciais de mídia de setor grande**

O setor de armazenamento está aumentando rapidamente os esforços para fazer a transição para esse novo tipo de formato avançado de armazenamento para mídia com um tamanho de setor físico de 4 KB. Dois tipos de mídia serão liberados para o mercado:

**4 KB nativos:** Esta mídia não tem camada de emulação e expõe diretamente 4 KB como seu tamanho de setor lógico e físico. O problema geral com esse novo tipo de mídia é que a maioria dos aplicativos e sistemas operacionais não consultam e alinham e/SS ao tamanho do setor físico, o que pode resultar em e/SS com falha inesperada.  
**emulação de 512 bytes (512e):** Esta mídia tem uma camada de emulação, conforme discutido na seção anterior, e expõe 512-bytes como seu tamanho de setor lógico (semelhante a um disco normal hoje), mas torna suas informações de tamanho de setor físico (4 KB) disponíveis. O problema geral com esse novo tipo de mídia é que a maioria dos aplicativos e sistemas operacionais não compreendem a existência do tamanho do setor físico, o que pode resultar em vários problemas, conforme será discutido abaixo.  
**suporte geral a Windows para mídia de setor grande**

Esta tabela documenta a política oficial de suporte da Microsoft para várias mídias e seus tamanhos de setor relatados resultantes. Consulte este [artigo da base de conhecimento](https://support.microsoft.com/kb/2510009) para obter detalhes.



| Nomes comuns                                  | Tamanho do setor lógico relatado | Tamanho do setor físico relatado | Windows Versão com suporte                                                                                                                                                                                                                                                                             |
|-----------------------------------------------|------------------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 512-byte nativo, 512n                         | 512 bytes                    | 512 bytes                     | Todas as versões do Windows                                                                                                                                                                                                                                                                                     |
| Formato avançado, 512e, AF, 512-emulação de byte | 512 bytes                    | 4 KB                          | Windows Vista w/MS KB 2553708 <br/> Windows Servidor 2008 \* w/MS KB 2553708 <br/> Windows 7 w/MS KB 982018 <br/> Windows Servidor 2008 R2 * w/MS KB 982018 <br/> todas as versões de Windows do Windows 7 SP1 e posteriores. <br/> Todas as versões do servidor do Server 2008 R2 SP1 e posteriores. <br/> <br/> \*Exceto para o Hyper-V. Consulte a seção ["requisitos de suporte de aplicativo para unidades de setor grande"](https://support.microsoft.com/help/2510009/microsoft-support-policy-for-4k-sector-hard-drives-in-windows) . |
| Formato avançado, AF, 4K nativo, 4Kn            | 4 KB                         | 4 KB                          | todas as versões de Windows de Windows 8 e posteriores <br/> todas as versões de servidor do Windows Server 2012 e posteriores <br/>                                                                                                                                                                                                                                                      |
| Outro                                         | Não 4 KB ou 512 bytes        | Não 4 KB ou 512 bytes         | Sem suporte                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> embora não esteja sob pressão na tabela anterior, Windows XP, Windows server 2003 e Windows server 2003 R2 não dão suporte à mídia 512e ou 4Kn. Embora o sistema possa ser inicializado e possa operar minimamente, pode haver cenários desconhecidos de problemas de funcionalidade, perda de dados ou desempenho abaixo do ideal. portanto, a Microsoft tem bastante cuidado com o uso de mídia 512e com Windows XP ou outros produtos baseados na base de código do Windows XP (como Windows Home Server 1,0, Windows server 2003, Windows server 2003 r2, Windows xp 64-bit Edition, Windows xp Embedded, Windows small business server 2003 e Windows small business server 2003 R2).

 

## <a name="how-emulation-works-read-modify-write-rmw"></a>Como a emulação funciona: Read-Modify-Write (RMW)

Uma mídia de armazenamento tem uma determinada unidade dentro da qual a mídia física pode ser modificada. Ou seja, a mídia só pode ser gravada ou reescrita, em unidades do tamanho do setor físico. Assim, as gravações não executadas nesse nível de unidade exigirão etapas adicionais, que veremos o exemplo abaixo.

Nesse cenário, um aplicativo precisa atualizar o conteúdo de um registro Datastor localizado em um setor lógico de 512 bytes. Este diagrama ilustra as etapas necessárias para que o dispositivo de armazenamento conclua a gravação:

![etapas para um dispositivo de armazenamento concluir uma gravação](images/512ermwsteps.png)

Conforme ilustrado acima, esse processo envolve algum trabalho pelo dispositivo de armazenamento que pode resultar em uma perda de desempenho. Para evitar esse trabalho adicional, os aplicativos devem ser atualizados para:

-   Consultar o tamanho do setor físico
-   Verifique se as gravações estão alinhadas ao tamanho do setor físico relatado

Embora isso inicialmente pareça ser apenas um problema de desempenho, pode haver um problema mais sério. Vamos discutir isso na próxima seção.

**Resiliência: o custo oculto de Read-Modify-Write**

A resiliência fala sobre a capacidade de um aplicativo de recuperar o estado entre as sessões. Vimos o que é necessário para um dispositivo de armazenamento 512e executar um setor de 512 byte gravar o ciclo de Leitura-Modificação-Gravação. Vamos ver o que aconteceria se o processo de substituição do setor físico anterior na mídia fosse interrompido. Quais seriam as consequências?

-   Como a maioria das unidades de disco rígido é atualizada no local, o setor físico, ou seja, a parte da mídia em que o setor físico estava localizado pode ter sido corrompida com informações incompletas devido a uma sobressalto parcial. Em outras condições, você pode pensar nisso como potencialmente tendo perdido todos os oito setores lógicos (que o setor físico contém logicamente).
-   Embora a maioria dos aplicativos com um armazenamento de dados seja projetada com a capacidade de se recuperar de erros de mídia, a perda de oito setores ou colocar outra maneira, a perda de oito registros de confirmação pode potencialmente tornar impossível para o armazenamento de dados a recuperação normalmente. Um administrador pode precisar restaurar manualmente o banco de dados de um backup ou até mesmo precisar executar uma recriação demorada.
-   Um impacto mais importante é que o ato de outro aplicativo que está causando um ciclo de Leitura-Modificação-Gravação pode potencialmente fazer com que seus dados sejam perdidos mesmo que seu aplicativo não seja executado! Isso é simplesmente porque os dados e os outros dados do aplicativo podem estar localizados no mesmo setor físico.

Com isso em mente, é importante que o software de aplicativo reavaliar quaisquer suposições feitas no código e estar ciente da distinção de tamanho do setor lógico-físico, juntamente com alguns cenários interessantes de clientes discutidos posteriormente neste artigo.

**Fazer a coisa certa (evitando leitura-modificação-gravação)**

Embora alguns fornecedores de armazenamento possam estar introduzindo alguns níveis de mitigação em determinados dispositivos de armazenamento do 512e para tentar facilitar o desempenho e os problemas de resiliência do ciclo de Leitura-Modificação-Gravação, há muito que qualquer mitigação pode lidar em termos de carga de trabalho. Dessa forma, os aplicativos não devem depender dessa mitigação como uma solução de longo prazo. Além disso, não há nenhuma garantia de que todas as classes de discos terão essa mitigação em curso, nem há uma garantia de que a mitigação seja bem projetada.

A solução para isso não é a mitigação na unidade, mas criar aplicativos para fazer o conjunto certo de coisas para ajudar a dar suporte a esse tipo de mídia. Esta seção aborda cenários comuns em que os aplicativos podem ter problemas com discos de setor grande e sugere uma via de investigação para tentar resolver cada problema.

**Problema 1: a partição não está alinhada a um limite de setor físico**

Quando o administrador/usuário particiona o disco, a primeira partição pode não ter sido criada em um limite alinhado. Isso pode fazer com que todas as gravações subsequentes se tornem não qualificadas para limites de setor físico. A partir do Windows Vista SP1 e Windows Server 2008, a primeira partição é colocada no primeiro 1024 KB do disco (para discos de 4 GB ou maior, caso contrário, o alinhamento é de 64 KB) alinhado a um limite de setor físico de 4 KB. No entanto, considerando o particionamento padrão no Windows XP, um utilitário de particionamento de terceiros ou o uso incorreto de APIs Windows, as partições criadas podem não estar alinhadas a um limite de setor físico. Os desenvolvedores precisarão garantir que as APIs corretas sejam usadas para ajudar a garantir o alinhamento. As APIs recomendadas para ajudar a garantir o alinhamento da partição são descritas abaixo.

As APIs IVdsPack::CreateVolume e IVdsPack2::CreateVolume2 não usam o parâmetro de alinhamento especificado quando um novo volume é criado, mas usam o valor de alinhamento padrão para o sistema operacional (o Pre-Windows Vista SP1 usará 63 bytes e o post Windows Vista SP1 usará os padrões mencionados acima). Em vez disso, use as APIs IVdsCreatePartitionEx::CreatePartitionEx ou IVdsAdvancedDisk::CreatePartition que usam o parâmetro de alinhamento especificado para os aplicativos que precisam criar partições.

A melhor maneira de ajudar a garantir que o alinhamento está correto é fazer isso corretamente ao criar inicialmente a partição. Caso contrário, seu aplicativo precisará levar em conta o alinhamento ao executar gravações ou na inicialização, o que pode ser um processo muito complexo.

**Problema 2: gravações sem-valor não alinhadas ao tamanho do setor físico**

O problema mais simples é que as gravações sem armazenamento não estão alinhadas ao tamanho do setor físico relatado da mídia de armazenamento. As gravações em buffer, por outro lado, são alinhadas ao tamanho da página de 4 KB, que coincidentemente é o tamanho do setor físico da primeira geração de mídia de grande setor. No entanto, a maioria dos aplicativos com um armazenamento de dados executa gravações sem armazenamento e, portanto, precisará garantir que essas gravações sejam executadas em unidades do tamanho do setor físico.

Alguns exemplos de cenários em que a E/S do aplicativo resultante não é não qualificada:

**Os registros de confirmação são padded para setores de 512 byte:** Os aplicativos com um armazenamento de dados normalmente têm alguma forma de registro de confirmação que mantém informações sobre alterações de metadados ou mantém a estrutura do armazenamento de dados. Para garantir que a perda de um setor não afete vários registros, esse registro de confirmação normalmente é preenchimento para um tamanho de setor. Com um disco com um tamanho de setor físico maior, o aplicativo precisará consultar o tamanho do setor físico, conforme mostrado na seção anterior, e garantir que cada registro de confirmação seja preenchimento para esse tamanho. Com um disco de 4K, isso garante que as E/Ss não falhem. Com um disco 512e, isso não apenas evita o ciclo de Leitura-Modificação-Gravação, mas ajuda a garantir que, se um setor físico fosse perdido, apenas um Registro de Confirmação seria perdido.  
**Os arquivos de log são gravados em partes não qualificadas:** A E/S não utilizada normalmente é usada ao atualizar ou fazer a aporte em um arquivo de log. Os aplicativos podem alternar para E/S em buffer ou buffer interno das atualizações de log para unidades do tamanho do setor físico para evitar E/Ss com falha ou disparar uma Leitura-Modificação/Gravação.  
 Para ajudar a determinar se seu aplicativo emite E/S sem buffer, inclua o sinalizador FILE FLAG NO BUFFERING no parâmetro \_ \_ \_ *dwFlagsAndAttributes* quando você chamar a função CreateFile.

Além disso, se você estiver alinhando atualmente as gravações ao tamanho do setor, esse tamanho de setor provavelmente será apenas o tamanho do setor lógico, pois a maioria das APIs existentes que consultam o tamanho do setor da mídia apenas consulta a unidade de endereçamento, ou seja, o tamanho do setor lógico. O tamanho do setor de interesse aqui é o tamanho do setor físico, que é a unidade real de atomicidade. Alguns exemplos de APIs que recuperam o tamanho do setor lógico são:

-   GetDiskFreeSpace, GetDiskFreeSpaceEx
-   FileFsVolumeInformation
-   IOCTL \_ DISK \_ GET \_ DRIVE \_ GEOMETRY, IOCTL \_ DISK \_ GET \_ DRIVE \_ GEOMETRY \_ EX
-   IVdsDisk::GetProperties, IVdsDisk3::GetProperties2

Veja como você pode consultar o tamanho do setor físico:

**Método preferencial para Windows 8**

Com Windows 8, a Microsoft introduziu uma nova API que permite aos desenvolvedores integrar facilmente o suporte a 4K em seus aplicativos. Essa nova API dá suporte a um número ainda maior de cenários do que o método herdado para Windows Vista e Windows 7 discutidos abaixo. Essa API habilita esses cenários de chamada:

-   Chamando de um aplicativo sem preço
-   Chamando para qualquer alça de arquivo válida
-   Chamando para um alçamento de arquivo em um volume remoto por SMB2
-   Modelo de programação simplificado

A API está na forma de uma nova classe de informações, FileFsSectorSizeInformation, com a estrutura associada FILE FS SECTOR SIZE INFORMATION, definida da \_ \_ seguinte \_ \_ maneira:


```
typedef struct _FILE_FS_SECTOR_SIZE_INFORMATION {  
    ULONG LogicalBytesPerSector;  
    ULONG PhysicalBytesPerSectorForAtomicity;  
    ULONG PhysicalBytesPerSectorForPerformance;  
    ULONG FileSystemEffectivePhysicalBytesPerSectorForAtomicity;  
    ULONG Flags;  
    ULONG ByteOffsetForSectorAlignment;  
    ULONG ByteOffsetForPartitionAlignment;  
} FILE_FS_SECTOR_SIZE_INFORMATION, *PFILE_FS_SECTOR_SIZE_INFORMATION;
```



**Método herddo para Windows 7 e Windows Vista**

Windows O Vista e Windows Server 2008 introduziram APIs para consultar o tamanho do setor físico do dispositivo de armazenamento anexado para controladores de armazenamento baseados em AHCI. Com Windows 7 e Windows Server 2008 R2, a partir do SP1 (ou Base de Dados de Conhecimento Microsoft 982018), esse suporte é estendido para controladores de armazenamento baseados em Storport. A Microsoft forneceu um [exemplo de código](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) no MSDN detalhando como um aplicativo pode consultar o tamanho do setor físico do volume.

Embora o exemplo de código acima permita obter o tamanho do setor físico do volume, você deve fazer algumas verificações básicas de integridade do tamanho do setor físico relatado antes de usá-lo, como foi observado que alguns drivers podem não retornar dados formatados corretamente:

-   Certifique-se de que o tamanho do setor físico relatado >= o tamanho do setor lógico relatado; se não for, seu aplicativo deverá usar um tamanho de setor físico igual ao tamanho do setor lógico relatado
-   Certifique-se de que o tamanho do setor físico relatado seja uma potência de dois; se não for, seu aplicativo deverá usar um tamanho de setor físico igual ao tamanho do setor lógico relatado
-   Se o tamanho do setor físico for um valor de potência de dois entre 512 bytes e 4 KB, considere usar um tamanho de setor físico arredondado para baixo até o tamanho do setor lógico relatado
-   Se o tamanho do setor físico for um valor de potência de dois maiores que 4 KB, você deverá avaliar a capacidade do aplicativo de lidar com esse cenário antes de usar esse valor; caso contrário, você deve considerar o uso de um tamanho de setor físico arredondado para baixo até 4 KB

Usar esse IOCTL para obter o tamanho do setor físico tem várias limitações. It:

-   Requer privilégios elevados; se o aplicativo não estiver em execução com privilégio, talvez seja necessário escrever um aplicativo Windows serviço, conforme mencionado acima
-   Não dá suporte a volumes SMB; talvez você também precise escrever um aplicativo de serviço Windows para dar suporte à consulta de tamanho de setor físico nesses volumes
-   Não pode ser emitido para qualquer alça de arquivo (o IOCTL deve ser emitido para um Alçamento de Volume)

**Problema 3: formatos de arquivo que dependem de setores de 512 byte**

Alguns aplicativos com formatos de arquivo padrão (como VHD 1.0) podem ter esses arquivos codificados para assumir um tamanho de setor de 512 byte. Portanto, as atualizações e gravações nesse arquivo resultariam em um ciclo de Leitura-Modificação-Gravação no dispositivo que potencialmente resultará em problemas de desempenho e resiliência para seus clientes. No entanto, há maneiras de um aplicativo fornecer suporte para operar nesse tipo de mídia, por exemplo:

-   Use o buffer para garantir que as gravações sejam executadas em unidades do tamanho do setor físico
-   Implementar uma Leitura-Modificação-Gravação interna que pode ajudar a garantir que as atualizações sejam executadas em unidades do tamanho do setor físico relatado
-   Se possível, pad registra em um setor físico, de forma que o preenchimento seja interpretado como espaço vazio
-   Considere recriar uma versão da estrutura de dados do aplicativo com suporte para setores maiores

**Problema 4: o tamanho do setor físico relatado pode mudar entre as sessões**

Há muitos cenários em que o tamanho do setor físico relatado do armazenamento subjacente que hospeda o Datastor pode mudar. O mais comum deles é quando você migra o Datastor para outro volume ou até mesmo pela rede. Uma alteração no tamanho do setor físico relatado pode ser um evento inesperado para muitos aplicativos e, potencialmente, pode fazer com que alguns aplicativos não sejam inicializados de novo.

Esse não é o cenário mais fácil de dar suporte e é mencionado aqui como uma consultoria. Você deve considerar os requisitos de mobilidade de seus clientes e ajustar seu suporte de acordo para ajudar a garantir que os clientes não sejam afetados negativamente usando mídia nativa de 4K ou 512e.

**Como um usuário pode recuperar o tamanho do setor lógico e físico para um volume**

A caixa de diálogo Windows é um utilitário para exibir as informações de tamanho do setor para um volume. As versões Windows com fsutil com suporte são:

-   Windows 8
-   Windows Server 2012
-   Windows 7 SP1 com o Microsoft KB 982018
-   Windows 7 com o Microsoft KB 982018
-   Windows Server 2008 R2 SP1 com o Microsoft KB 982018 (v3)
-   Windows Server 2008 R2 com o Microsoft KB 982018 (v3)
-   Windows Vista com o Microsoft KB 2553708
-   Windows Server 2008 com o Microsoft KB 2553708

Para obter as informações de tamanho do setor, chame o utilitário da seguinte forma em um prompt de comando elevado:


```
fsutil fsinfo ntfsinfo <drive letter>
```



Um Disco de Setor de 4K com emulação de 512 bytes tem o campo Bytes por Setor definido como 512 e o campo Bytes por Setor Físico definido como 4096 da seguinte forma:

![bytes por setor e por setor físico de um disco de setor de 4k com emulação de 512 bytes](images/4ksectordiskwith512emulation.png)

Um disco nativo de 4K tem os campos Bytes por Setor e Bytes por Setor Físico definidos como 4096 da seguinte forma:

![bytes por setor e por setor físico de um disco nativo de 4k](images/4knativedisk.png)

> [!Note]  
> Se o campo Byte por Setor Físico exibir Sem Suporte, o driver de armazenamento não dá suporte à PROPRIEDADE DE CONSULTA DE ARMAZENAMENTO IOCTL ou houve um erro ao recuperar as \_ \_ \_ informações.

 

## <a name="resources"></a>Recursos

-   [Windows Instrução de suporte geral](https://support.microsoft.com/kb/2510009)
-   [Microsoft KB 982018](https://support.microsoft.com/kb/982018)
-   [Microsoft KB 2553708](https://support.microsoft.com/kb/2553708)
-   [Hotfix para Windows 7 e Windows Server 2008 R2](https://support.microsoft.com/kb/982018)
-   [Hotfix para Windows Vista e Windows Server 2008](https://support.microsoft.com/kb/2553708)
-   [Instrução de suporte do HyperV](https://support.microsoft.com/kb/2515143)
-   [Informações gerais sobre o código de controle IOCTL \_ STORAGE \_ QUERY \_ PROPERTY](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   [Código de controle de PROPRIEDADE \_ \_ DE CONSULTA DE \_ ARMAZENAMENTO IOCTL](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   [Informações gerais sobre a estrutura DO \_ \_ DESCRITOR DE ALINHAMENTO DE ACESSO \_ AO ARMAZENAMENTO](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   [Descrição da terminologia padrão usada para descrever as atualizações de software da Microsoft](https://support.microsoft.com/kb/824684/)
-   [Código de exemplo do WDK com detalhes sobre como extrair as informações de alinhamento de acesso de armazenamento relatadas da estrutura DESCRIPTOR DE ALINHAMENTO DE ACESSO AO ARMAZENAMENTO ao fazer uma chamada para o código de controle \_ \_ \_ IOCTL \_ STORAGE \_ QUERY \_ PROPERTY](/windows/win32/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   [Informações gerais sobre as ImageX Command-Line opções](/previous-versions/windows/it-pro/windows-7/dd799302(v=ws.10))
-   [Requisitos de driver do Intel Chipset para dar suporte a unidades de setor de 4 KB](https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm)

 

