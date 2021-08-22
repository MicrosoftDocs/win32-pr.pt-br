---
description: este tópico apresenta o efeito de dispositivos de armazenamento de formato avançado em software, discute o que os aplicativos podem fazer para ajudar a dar suporte a esse tipo de mídia e discute a infraestrutura que a Microsoft introduziu com o Windows 7 SP1 e o Windows Server 2008 R2 SP1 para permitir que os desenvolvedores ofereçam suporte a esses tipos de dispositivos.
ms.assetid: 1D2847A7-15E9-42E0-90EB-7F43E76D3E44
title: Atualização de compatibilidade de disco do 512e (emulação de 512 bytes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd26cfe1b5417af75906431291a51650757c08464f0c1dc6966ef7f58223423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134169"
---
# <a name="512-byte-emulation-512e-disk-compatibility-update"></a>Atualização de compatibilidade de disco do 512e (emulação de 512 bytes)

## <a name="platform"></a>Plataforma

 **clientes** -Windows Vista, Windows 7, Windows 7 SP1  
**servidores** -Windows server 2008, Windows server 2008 r2, Windows server 2008 r2 SP1  

## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -alta  
**Frequência** -alta  









## <a name="description"></a>Descrição

As densidades areais estão cada vez mais anuais e com o surgimento recente de 3 TB de discos, os mecanismos de correção de erros usados para lidar com a proporção de sinais-to-Noise (SNR) não estão ficando ineficientes – ou seja, uma maior quantidade de sobrecarga é necessária para garantir que a mídia seja utilizável. Uma das soluções do setor de armazenamento para melhorar esse mecanismo de correção de erros é introduzir um formato de mídia físico diferente que inclua um tamanho de setor físico maior. Esse novo formato de mídia física é chamado de *formato avançado*. Portanto, não é mais seguro fazer suposições sobre o tamanho do setor de dispositivos de armazenamento modernos, e os desenvolvedores precisarão estudar as suposições subjacentes a seu código para determinar se há um impacto.

Este tópico apresenta o efeito de dispositivos de armazenamento de formato avançado em software, discute o que os aplicativos podem fazer para ajudar a dar suporte a esse tipo de mídia e discute a infraestrutura para permitir que os desenvolvedores ofereçam suporte a esses tipos de dispositivos. Embora o material apresentado neste tópico forneça diretrizes para melhorar a compatibilidade com discos de formato avançado, as informações aplicam-se geralmente a todos os sistemas com discos de formato avançados. as seguintes versões do Windows fornecem suporte para consultar o tamanho do setor físico:

-   Windows 7 com Microsoft KB 982018
-   Windows 7 SP1
-   Windows Server 2008 R2 com Microsoft KB 982018
-   Windows Server 2008 R2 SP1
-   Windows Vista com Microsoft KB 2553708
-   Windows Servidor 2008 com Microsoft KB 2553708

Para obter detalhes adicionais, consulte [informações sobre a política de suporte da Microsoft para unidades de grandes setores no Windows](https://support.microsoft.com/kb/2510009).

Para obter mais informações sobre discos de formato avançado, entre em contato com seu fornecedor de armazenamento.

## <a name="logical-vs-physical-sector-size"></a>Tamanho lógico vs. de setor físico

Uma das preocupações na introdução dessa alteração no formato de mídia é a compatibilidade com o software e o hardware atualmente disponíveis no mercado atualmente. Como uma solução temporária, a indústria de armazenamento está inicialmente introduzindo discos que emulam um disco de setor de 512 bytes comum, mas disponibilizam informações sobre o tamanho real do setor por meio de comandos ATA e SCSI padrão. Como resultado dessa emulação, há dois tamanhos de setor:

-   **Setor lógico**: a unidade usada para endereçamento de bloco lógico para a mídia. Também podemos considerar isso como a menor unidade de gravação que o armazenamento pode aceitar. Esta é a emulação.

-   **Setor físico**: a unidade para a qual as operações de leitura e gravação para o dispositivo são concluídas em uma única operação. Esta é a unidade de gravação atômica.

a maioria das APIs de Windows atuais, como o **disco de IOCTL \_ \_ obter \_ \_ geometria de unidade** retornará o tamanho do setor lógico, mas o tamanho do setor físico pode ser recuperado por meio do código de controle de [ \_ \_ \_ propriedade de consulta de armazenamento do ioctl](/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property) , com as informações relevantes contidas no campo **BytesPerPhysicalSector** na estrutura do [ \_ \_ \_ descritor de alinhamento de acesso de armazenamento](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) . Isso é discutido em mais detalhes posteriormente neste artigo.

## <a name="initial-types-of-large-sector-media"></a>Tipos iniciais de mídia de setor grande

O setor de armazenamento está aumentando rapidamente os esforços para fazer a transição para esse novo tipo de formato avançado de armazenamento para mídia com tamanhos de setor físico de 4 KB. Dois tipos de mídia serão liberados para o mercado:

-   **4 KB nativo**: essa mídia não tem uma camada de emulação e expõe diretamente 4 KB como seu tamanho de setor lógico e físico. atualmente, essa mídia não é compatível com Windows e com a maioria dos outros sistemas operacionais. no entanto, a Microsoft está realizando uma investigação da viabilidade de dar suporte a esse tipo de mídia em uma versão futura do Windows e emitirá um artigo da Base de dados de conhecimento quando for apropriado.
-   **emulação de 512 bytes (512e)**: essa mídia tem uma camada de emulação conforme abordada na seção anterior e expõe 512-bytes como seu tamanho de setor lógico (semelhante a um disco normal hoje), mas disponibiliza suas informações de tamanho de setor físico (4 KB). Isso é o que vários fornecedores de armazenamento estão apresentando atualmente ao mercado. Esse problema geral com esse novo tipo de mídia é que a maioria dos aplicativos e sistemas operacionais não compreendem a existência do tamanho do setor físico, o que pode resultar em vários problemas, conforme será discutido abaixo.

## <a name="how-emulation-works-read-modify-write-rmw"></a>Como a emulação funciona: Read-Modify-Write (RMW)

Uma mídia de armazenamento tem uma determinada unidade dentro da qual a mídia física pode ser modificada. Ou seja, a mídia só pode ser gravada ou reescrita, em unidades do tamanho do setor físico. Assim, as gravações não executadas nesse nível de unidade exigirão etapas adicionais, que veremos no exemplo a seguir.

Nesse cenário, um aplicativo precisa atualizar o conteúdo de um registro Datastor localizado em um setor lógico de 512 bytes. O diagrama a seguir ilustra as etapas necessárias para que o dispositivo de armazenamento conclua a gravação:

![etapas necessárias para atualizar o registro Datastor dentro de um setor lógico de 512 bytes](images/512ermwsteps.png)

Conforme ilustrado acima, esse processo envolve algum trabalho pelo dispositivo de armazenamento que pode resultar em uma perda de desempenho. Para evitar esse trabalho adicional, os aplicativos devem ser atualizados para fazer o seguinte:

-   Consultar o tamanho do setor físico.
-   Verifique se as gravações estão alinhadas ao tamanho do setor físico relatado.

## <a name="the-resiliency-impact-of-read-modify-write"></a>O impacto de resiliência de Read-Modify-Write

A resiliência fala sobre a capacidade de um aplicativo de recuperar o estado entre as sessões. Vimos o que é necessário para um dispositivo de armazenamento 512e executar uma gravação de setor de 512 bytes – o ciclo de leitura-modificação-gravação. Vamos examinar o que aconteceria se o processo de substituição do setor físico anterior na mídia fosse interrompido. Quais seriam as consequências?

-   Como a maioria das unidades de disco rígido é atualizada no local, o setor físico – ou seja, a parte da mídia em que o setor físico estava localizado – poderia ter sido corrompido com informações incompletas devido a uma substituição parcial. Em outras palavras, você pode imaginar como potencialmente ter perdido todos os 8 setores lógicos (que o setor físico contém logicamente).

-   Embora a maioria dos aplicativos com um armazenamento de dados seja projetada com a capacidade de se recuperar de erros de mídia, a perda de oito setores ou colocar outra maneira, a perda de oito registros de confirmação, pode potencialmente torná-lo impossível para que o armazenamento de dados se recupere normalmente. Um administrador pode precisar restaurar manualmente o banco de dados de um backup ou pode até mesmo precisar executar uma recompilação demorada.

-   Um impacto mais importante é que o ato de outro aplicativo causando um ciclo de leitura-modificação-gravação pode potencialmente causar a perda dos dados, mesmo que seu aplicativo não esteja em execução! Isso é simplesmente porque seus dados e os dados do outro aplicativo podem estar localizados no mesmo setor físico.

Com isso em mente, é importante que o software de aplicativo reavalie as suposições tomadas no código e esteja atento à distinção de tamanho de setor físico lógico, juntamente com alguns cenários de clientes interessantes discutidos posteriormente neste artigo.

É mais provável que esse problema ocorra se seu aplicativo depender de um armazenamento de dados de estrutura de log.

## <a name="avoiding-read-modify-write"></a>Evitando leitura-modificar-gravar

Embora alguns fornecedores de armazenamento possam estar apresentando alguns níveis de mitigação em determinados dispositivos de armazenamento 512e para tentar e ajudar a facilitar os problemas de desempenho e resiliência do ciclo de leitura-modificação-gravação, há apenas que qualquer mitigação pode lidar em termos de carga de trabalho. Dessa forma, os aplicativos não devem depender dessa mitigação como uma solução de longo prazo.

A solução para isso não é mitigação na unidade, mas para que os aplicativos façam o conjunto certo de coisas para evitar o ciclo de leitura-modificação-gravação. Esta seção aborda cenários comuns em que os aplicativos podem ter problemas com discos de setor grande e sugere uma avenida de investigação para tentar resolver cada problema.

### <a name="issue-1-the-partition-is-not-aligned-to-a-physical-sector-boundary"></a>Problema 1: a partição não está alinhada a um limite de setor físico

Quando o administrador/usuário particiona o disco, a primeira partição pode não ter sido criada em um limite alinhado. Isso pode fazer com que todas as gravações subsequentes fiquem desalinhadas aos limites do setor físico. a partir do Windows Vista SP1 e do Windows Server 2008, a primeira partição é colocada no primeiro 1024 kb do disco (para discos de 4 gb ou maiores, caso contrário, o alinhamento é 64 kb) que está alinhado a um limite de setor físico de 4 KB. no entanto, considerando o particionamento padrão no Windows XP, um utilitário de particionamento de terceiros ou uso incorreto de APIs de Windows, as partições criadas não podem ser alinhadas a um limite de setor físico. Os desenvolvedores precisarão garantir que as APIs corretas sejam usadas para ajudar a garantir o alinhamento. As APIs recomendadas para ajudar a garantir que o alinhamento da partição seja descrito abaixo.

as APIs **IVdsPack:: createvolume** e **IVdsPack2:: CreateVolume2** não usam o parâmetro de alinhamento especificado quando um novo volume é criado e, em vez disso, usam o valor de alinhamento padrão para o sistema operacional (pré Windows o vista sp1 usará 63 bytes e o post Windows vista sp1 usará os padrões declarados acima). Portanto, é recomendável que os aplicativos que precisam criar partições usem as APIs **IVdsCreatePartitionEx:: CreatePartitionEx** ou **IVdsAdvancedDisk:: CreatePartition** , que usam o parâmetro de alinhamento especificado.

A melhor maneira de ajudar a garantir que o alinhamento esteja correto é fazer isso corretamente ao criar inicialmente a partição. Caso contrário, seu aplicativo precisará colocar o alinhamento em conta ao executar gravações ou na inicialização – o que pode ser uma questão muito complexa. a partir do Windows Vista SP1, isso geralmente não é um problema; no entanto, as versões mais antigas do Windows podem criar partições não alinhadas que podem potencialmente causar problemas de desempenho com alguns discos de formato avançados.

### <a name="issue-2-unbuffered-writes-not-aligned-to-physical-sector-size"></a>Problema 2: gravações sem buffer não alinhadas ao tamanho do setor físico

O problema básico é que as gravações sem buffer não estão alinhadas ao tamanho do setor físico relatado da mídia de armazenamento, o que dispara uma leitura-modificação-gravação na unidade que pode resultar em problemas de desempenho. Gravações em buffer, por outro lado, são alinhadas ao tamanho da página – 4 KB – que coincidente é o tamanho do setor físico da primeira geração de mídia de setor grande. No entanto, a maioria dos aplicativos com um armazenamento de dados executa gravações sem buffer e, portanto, precisará garantir que essas gravações sejam executadas em unidades do tamanho do setor físico.

Para ajudar a determinar se seu aplicativo emite e/s sem buffer, verifique se você incluiu o sinalizador **File \_ Flag \_ no \_ buffer** no parâmetro *dwFlagsAndAttributes* ao chamar a função **CreateFile** .

Além disso, se você estiver alinhando as gravações no tamanho do setor, esse tamanho de setor provavelmente será apenas o tamanho do setor *lógico* , já que a maioria das APIs existentes que consultam o tamanho do setor da mídia, na verdade, apenas consulta a unidade de endereçamento – ou seja, o tamanho do setor lógico. O tamanho do setor de interesse aqui é o tamanho do setor físico, que é a unidade real de atomicidade. Alguns exemplos de APIs que recuperam o tamanho do setor lógico são:

-   **GetDiskFreeSpace**, **GetDiskFreeSpaceEx**
-   **FileFsVolumeInformation**
-   **IOCTL \_ DISCO \_ obter \_ \_ geometria da unidade**, disco do **IOCTL \_ \_ obter geometria da \_ unidade \_ \_ ex** .
-   **IVdsDisk:: GetProperties**, **IVdsDisk3:: GetProperties2**

**Como consultar o tamanho do setor físico**

A Microsoft forneceu um exemplo de código no MSDN detalhando como um aplicativo pode consultar o tamanho do setor físico do volume. O exemplo de código está localizado em <https://msdn.microsoft.com/library/ff800831.aspx> .

Embora o exemplo de código acima permita obter o tamanho do setor físico do volume, você deve fazer algumas verificações básicas de integridade sobre o tamanho do setor físico relatado antes de usá-lo, como foi observado que alguns drivers podem não retornar dados formatados corretamente:

-   Certifique-se de que o tamanho do setor físico relatado >= o tamanho do setor lógico relatado. Se não estiver, seu aplicativo deverá usar um tamanho de setor físico igual ao tamanho do setor lógico relatado.
-   Certifique-se de que o tamanho do setor físico relatado seja uma potência de dois. Se não estiver, seu aplicativo deverá usar um tamanho de setor físico igual ao tamanho do setor lógico relatado.
-   Se o tamanho do setor físico for um valor de potência de dois entre 512 bytes e 4 KB, considere usar um tamanho de setor físico arredondado para baixo até o tamanho do setor lógico relatado.
-   Se o tamanho do setor físico for um valor de potência de dois maiores que 4 KB, você deverá avaliar a capacidade do aplicativo de lidar com esse cenário antes de usar esse valor. Caso contrário, você deve considerar o uso de um tamanho de setor físico arredondado para 4 KB.

O uso desse IOCTL para obter o tamanho do setor físico tem várias limitações:

-   Requer privilégios elevados. Se o aplicativo não estiver em execução com privilégio, talvez seja necessário escrever um aplicativo Windows serviço, conforme mencionado acima.

-   Não dá suporte a volumes SMB. Talvez você também precise escrever um aplicativo de serviço Windows para dar suporte à consulta de tamanho de setor físico nesses volumes.

-   Não pode ser emitido para qualquer alça de arquivo (o IOCTL deve ser emitido para um Alçamento de Volume).

-   Com suporte apenas em Windows versões listadas perto do início deste artigo.

**Os registros de confirmação são padded para setores de 512 byte**

Aplicativos com um armazenamento de dados normalmente têm alguma forma de registro de confirmação que mantém informações sobre alterações de metadados ou mantém a estrutura do armazenamento de dados. Para garantir que a perda de um setor não afete vários registros, esse registro de confirmação normalmente é preenchimento para um tamanho de setor. Com um disco com um tamanho de setor físico maior, o aplicativo precisará consultar o tamanho do setor físico, conforme mostrado na seção anterior, e garantir que cada registro de confirmação seja preenchimento para esse tamanho. Isso não apenas evita o ciclo de Leitura-Modificação-Gravação, mas também ajuda a garantir que, no caso de perda de um setor físico, apenas um Registro de Confirmação seria perdido.

**Os arquivos de log são gravados em partes não qualificadas**

A E/S não utilizada normalmente é usada ao atualizar ou se conectar a um arquivo de log. Há várias maneiras de ajudar a garantir que essas atualizações estejam alinhadas corretamente:

-   Internamente, o buffer de atualizações de log para o tamanho do setor físico relatado da mídia operacional e as gravações de log de emissão somente quando uma unidade de setor físico está cheia
-   Usar E/S em buffer

### <a name="issue-3-file-formats-relying-on-512-byte-sectors"></a>Problema 3: Formatos de arquivo que dependem de setores de 512 byte

Alguns aplicativos com formatos de arquivo padrão (como VHD 1.0) podem ter esses arquivos codificados para assumir um tamanho de setor de 512 byte. Portanto, as atualizações e gravações nesse arquivo resultariam em um ciclo de Leitura-Modificação-Gravação no dispositivo, o que potencialmente resultará em preocupações de desempenho e resiliência para seus clientes. No entanto, há maneiras de um aplicativo fornecer suporte para operar nesse tipo de mídia, por exemplo:

-   Use o buffer para garantir que as gravações sejam executadas em unidades do tamanho do setor físico
-   Implementar uma Leitura-Modificação-Gravação interna que pode ajudar a garantir que as atualizações sejam executadas em unidades do tamanho do setor físico relatado
-   Se possível, pad registra em um setor físico, de forma que o preenchimento seja interpretado como espaço vazio
-   Considere recriar uma nova versão da estrutura de dados do aplicativo com suporte para setores maiores

### <a name="issue-4-the-reported-physical-sector-size-can-change-between-sessions"></a>Problema 4: o tamanho do setor físico relatado pode mudar entre as sessões

Há muitos cenários em que o tamanho do setor físico relatado do armazenamento subjacente que hospeda o Datastor pode mudar. O mais comum deles é quando você migra o Datastor para outro volume ou até mesmo pela rede. Uma alteração no tamanho do setor físico relatado pode ser um evento inesperado para muitos aplicativos e potencialmente pode resultar em alguns aplicativos até mesmo falhando na inicialização.

Esse não é o cenário mais fácil de dar suporte e é mencionado aqui como uma consultoria. Você deve considerar os requisitos de mobilidade de seus clientes e ajustar seu suporte de acordo para ajudar a garantir que os clientes não sejam afetados negativamente usando a mídia 512e.

## <a name="4-kb-native-media"></a>Mídia nativa de 4 KB

A mídia de emulação de 512 byte é destinada como uma etapa de transição entre a mídia nativa de 512 byte e a mídia nativa de 4 KB, e esperamos ver uma mídia nativa de 4 KB lançada logo após a disponibilização do 512e. Há várias implicações importantes com essa mídia que devem ser notadas:

-   Os tamanhos de setor lógico e físico são de 4 KB
-   Como não há nenhuma camada de emulação, as gravações não não qualificadas falharão pelo armazenamento
-   Nenhum acerto de resiliência oculto – os aplicativos funcionam ou não funcionam

Embora a Microsoft atualmente está investigando o suporte para esses tipos de mídia em uma versão futura do Windows e emitirá um artigo de KB quando apropriado, os desenvolvedores de aplicativos devem considerar fornecer suporte preventivamente para esses tipos de mídia.

## <a name="closing"></a>Fechamento

Neste artigo, discutimos os afeta que a mídia de grande setor apresenta com muitos cenários comuns de implantação. Vimos o impacto no desempenho e na resiliência de Leitura-Modificação-Gravação, alguns dos cenários interessantes que essa mídia pode apresentar e o conjunto de problemas que eles podem causar com o software, o que, por fim, afeta o usuário final. O setor de armazenamento está rapidamente em transição para mídia com tamanhos de setor maiores e, muito em breve, os clientes não poderão comprar discos com tamanhos tradicionais de setor de 512 byte.

Este é um documento vivo e é destinado a ajudar os desenvolvedores a entenderem essa transição. Você deve iniciar uma conversa com suas respectivas organizações, com clientes, profissionais de TI e seus fornecedores de hardware para falar sobre a transição de setor grande e como ela afeta os cenários que são importantes para você.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   **Windows de suporte geral:**<https://support.microsoft.com/kb/2510009>
-   **Hotfix para Windows 7 e Windows Server 2008 R2:**<https://support.microsoft.com/kb/982018>
-   **Hotfix para Windows Vista e Windows Server 2008:**<https://support.microsoft.com/kb/2470478>
-   **Instrução de suporte do HyperV:**<https://support.microsoft.com/kb/2515143>
-   **Informações gerais sobre o IOCTL \_ Código de controle STORAGE \_ QUERY \_ PROPERTY**: [https://msdn.microsoft.com/library/ff560590.aspx](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   **IOCTL \_ Código \_ de controle DE PROPRIEDADE DE CONSULTA DE \_ ARMAZENAMENTO**: [https://msdn.microsoft.com/library/ff800830.aspx](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   **Informações gerais sobre o ARMAZENAMENTO \_ Estrutura \_ \_ DO DESCRITOR DE ALINHAMENTO DE ACESSO**: [https://msdn.microsoft.com/library/ff566344.aspx](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   **Descrição da terminologia padrão usada para descrever as atualizações de software da Microsoft:**<https://support.microsoft.com/kb/824684/>
-   Código de exemplo do **WDK** com detalhes sobre como extrair as informações de alinhamento de acesso de armazenamento relatadas da estrutura **STORAGE ACCESS ALIGNMENT \_ \_ \_ DESCRIPTOR** ao fazer uma chamada para o código de controle **IOCTL \_ STORAGE \_ QUERY \_ PROPERTY:** [/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   **Informações gerais sobre as ImageX Command-Line opções**:<https://technet.microsoft.com/library/dd799302(WS.10).aspx>
-   **Requisitos de driver do Intel Chipset para dar suporte a unidades de setor de 4 KB:**<https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm>
-   Para obter mais informações sobre Discos de Formato Avançado, visite os seguintes sites do IDEMA:
    -   <http://idema.org/?page_id=2172>
    -   <http://idema.org/?download=7926>

 

 
