---
description: Este tópico apresenta o efeito de dispositivos de armazenamento de formato avançado em software, discute o que os aplicativos podem fazer para ajudar a dar suporte a esse tipo de mídia e discute a infraestrutura que a Microsoft introduziu com o Windows 7 SP1 e o Windows Server 2008 R2 SP1 para permitir que os desenvolvedores ofereçam suporte a esses tipos de dispositivos.
ms.assetid: 1D2847A7-15E9-42E0-90EB-7F43E76D3E44
title: Atualização de compatibilidade de disco do 512e (emulação de 512 bytes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b654473fa8be5fbea997bd063df2c1f898a7d1
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314999"
---
# <a name="512-byte-emulation-512e-disk-compatibility-update"></a>Atualização de compatibilidade de disco do 512e (emulação de 512 bytes)

## <a name="platform"></a>Plataforma

 **Clientes** -Windows Vista, Windows 7, Windows 7 SP1  
**Servidores** -windows Server 2008, windows Server 2008 R2, windows Server 2008 R2 SP1  

## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -alta  
**Frequência** -alta  









## <a name="description"></a>Descrição

As densidades areais estão cada vez mais anuais e com o surgimento recente de 3 TB de discos, os mecanismos de correção de erros usados para lidar com a proporção de sinais-to-Noise (SNR) não estão ficando ineficientes – ou seja, uma maior quantidade de sobrecarga é necessária para garantir que a mídia seja utilizável. Uma das soluções do setor de armazenamento para melhorar esse mecanismo de correção de erros é introduzir um formato de mídia físico diferente que inclua um tamanho de setor físico maior. Esse novo formato de mídia física é chamado de *formato avançado*. Portanto, não é mais seguro fazer suposições sobre o tamanho do setor de dispositivos de armazenamento modernos, e os desenvolvedores precisarão estudar as suposições subjacentes a seu código para determinar se há um impacto.

Este tópico apresenta o efeito de dispositivos de armazenamento de formato avançado em software, discute o que os aplicativos podem fazer para ajudar a dar suporte a esse tipo de mídia e discute a infraestrutura para permitir que os desenvolvedores ofereçam suporte a esses tipos de dispositivos. Embora o material apresentado neste tópico forneça diretrizes para melhorar a compatibilidade com discos de formato avançado, as informações aplicam-se geralmente a todos os sistemas com discos de formato avançados. As seguintes versões do Windows fornecem suporte para consultar o tamanho do setor físico:

-   Windows 7 com Microsoft KB 982018
-   Windows 7 SP1
-   Windows Server 2008 R2 com Microsoft KB 982018
-   Windows Server 2008 R2 SP1
-   Windows Vista com Microsoft KB 2553708
-   Windows Server 2008 com Microsoft KB 2553708

Para obter detalhes adicionais, consulte [informações sobre a política de suporte da Microsoft para unidades de grandes setores no Windows](https://support.microsoft.com/kb/2510009).

Para obter mais informações sobre discos de formato avançado, entre em contato com seu fornecedor de armazenamento.

## <a name="logical-vs-physical-sector-size"></a>Tamanho lógico vs. de setor físico

Uma das preocupações na introdução dessa alteração no formato de mídia é a compatibilidade com o software e o hardware atualmente disponíveis no mercado atualmente. Como uma solução temporária, a indústria de armazenamento está inicialmente introduzindo discos que emulam um disco de setor de 512 bytes comum, mas disponibilizam informações sobre o tamanho real do setor por meio de comandos ATA e SCSI padrão. Como resultado dessa emulação, há dois tamanhos de setor:

-   **Setor lógico**: a unidade usada para endereçamento de bloco lógico para a mídia. Também podemos considerar isso como a menor unidade de gravação que o armazenamento pode aceitar. Esta é a emulação.

-   **Setor físico**: a unidade para a qual as operações de leitura e gravação para o dispositivo são concluídas em uma única operação. Esta é a unidade de gravação atômica.

A maioria das APIs do Windows atuais, como o disco do IOCTL, a **\_ \_ \_ \_ geometria da unidade** retornará o tamanho do setor lógico, mas o tamanho do setor físico pode ser recuperado por meio do código de controle da [ \_ \_ \_ propriedade de consulta de armazenamento do IOCTL](/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property) , com as informações relevantes contidas no campo **BytesPerPhysicalSector** na estrutura do [ \_ \_ \_ descritor de alinhamento de acesso de armazenamento](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) . Isso é discutido em mais detalhes posteriormente neste artigo.

## <a name="initial-types-of-large-sector-media"></a>Tipos iniciais de mídia de setor grande

O setor de armazenamento está aumentando rapidamente os esforços para fazer a transição para esse novo tipo de formato avançado de armazenamento para mídia com tamanhos de setor físico de 4 KB. Dois tipos de mídia serão liberados para o mercado:

-   **4 KB nativo**: essa mídia não tem uma camada de emulação e expõe diretamente 4 KB como seu tamanho de setor lógico e físico. Atualmente, essa mídia não é compatível com o Windows e com a maioria dos outros sistemas operacionais. No entanto, a Microsoft está realizando uma investigação da viabilidade de dar suporte a esse tipo de mídia em uma versão futura do Windows e emitirá um artigo da base de dados de conhecimento, quando apropriado.
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

Quando o administrador/usuário particiona o disco, a primeira partição pode não ter sido criada em um limite alinhado. Isso pode fazer com que todas as gravações subsequentes fiquem desalinhadas aos limites do setor físico. A partir do Windows Vista SP1 e do Windows Server 2008, a primeira partição é colocada no primeiro 1024 KB do disco (para discos de 4 GB ou maiores, caso contrário, o alinhamento é 64 KB) que está alinhado a um limite de setor físico de 4 KB. No entanto, considerando o particionamento padrão no Windows XP, um utilitário de particionamento de terceiros ou um uso incorreto de APIs do Windows, as partições criadas não podem ser alinhadas a um limite de setor físico. Os desenvolvedores precisarão garantir que as APIs corretas sejam usadas para ajudar a garantir o alinhamento. As APIs recomendadas para ajudar a garantir que o alinhamento da partição seja descrito abaixo.

As APIs **IVdsPack:: createvolume** e **IVdsPack2:: CreateVolume2** não usam o parâmetro de alinhamento especificado quando um novo volume é criado e, em vez disso, usam o valor de alinhamento padrão para o sistema operacional (pré-Windows Vista SP1 usará 63 bytes, e o post Windows Vista SP1 usará os padrões declarados acima). Portanto, é recomendável que os aplicativos que precisam criar partições usem as APIs **IVdsCreatePartitionEx:: CreatePartitionEx** ou **IVdsAdvancedDisk:: CreatePartition** , que usam o parâmetro de alinhamento especificado.

A melhor maneira de ajudar a garantir que o alinhamento esteja correto é fazer isso corretamente ao criar inicialmente a partição. Caso contrário, seu aplicativo precisará colocar o alinhamento em conta ao executar gravações ou na inicialização – o que pode ser uma questão muito complexa. A partir do Windows Vista SP1, isso geralmente não é um problema; no entanto, as versões mais antigas do Windows podem criar partições não alinhadas que podem potencialmente causar problemas de desempenho com alguns discos de formato avançados.

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

Embora o exemplo de código acima permita que você obtenha o tamanho do setor físico do volume, você deve fazer alguma verificação de sanidade básica no tamanho do setor físico relatado antes de usá-lo, já que alguns drivers podem não retornar dados formatados corretamente:

-   Verifique se o tamanho do setor físico relatado é >= o tamanho do setor lógico relatado. Se não for, seu aplicativo deverá usar um tamanho de setor físico igual ao tamanho de setor lógico relatado.
-   Verifique se o tamanho do setor físico relatado é uma potência de dois. Se não for, seu aplicativo deverá usar um tamanho de setor físico igual ao tamanho de setor lógico relatado.
-   Se o tamanho do setor físico for um valor de potência de dois entre 512 bytes e 4 KB, você deverá considerar o uso de um tamanho de setor físico arredondado para baixo até o tamanho de setor lógico relatado.
-   Se o tamanho do setor físico for um valor de mais de 4 KB, você deverá avaliar a capacidade do seu aplicativo de lidar com esse cenário antes de usar esse valor. Caso contrário, você deve considerar o uso de um tamanho de setor físico arredondado para 4 KB.

O uso deste IOCTL para obter o tamanho do setor físico tem várias limitações:

-   Requer privilégio elevado. Se o seu aplicativo não estiver sendo executado com privilégios, talvez seja necessário escrever um aplicativo de serviço do Windows, conforme indicado acima.

-   Não oferece suporte a volumes SMB. Talvez você também precise escrever um aplicativo de serviço do Windows para dar suporte à consulta de tamanho de setor físico nesses volumes.

-   Não pode ser emitido para nenhum identificador de arquivo (o IOCTL deve ser emitido para um identificador de volume).

-   Com suporte apenas em versões do Windows listadas próximo ao início deste artigo.

**Os registros de confirmação são preenchidos em setores de 512 bytes**

Aplicativos com um armazenamento de dados normalmente têm alguma forma de registro de confirmação que mantém informações sobre alterações de metadados ou mantém a estrutura do armazenamento de dados. Para garantir que a perda de um setor não afete vários registros, esse registro de confirmação normalmente é preenchido para um tamanho de setor. Com um disco com um tamanho de setor físico maior, o aplicativo precisará consultar o tamanho do setor físico, conforme mostrado na seção anterior, e garantir que cada registro de confirmação seja preenchido para esse tamanho. Isso não apenas evita o ciclo de leitura-modificação-gravação, ajuda a garantir que, caso um setor físico tenha sido perdido, apenas um registro de confirmação seria perdido.

**Os arquivos de log são gravados em partes não alinhadas**

A e/s não armazenada em buffer normalmente é usada ao atualizar ou anexar a um arquivo de log. Há várias maneiras de ajudar a garantir que essas atualizações estejam alinhadas corretamente:

-   Atualizações de log de buffer internamente para o tamanho de setor físico relatado da mídia operacional e problemas de gravação de log somente quando uma unidade de setor físico estiver cheia
-   Usar e/s em buffer

### <a name="issue-3-file-formats-relying-on-512-byte-sectors"></a>Problema 3: os formatos de arquivo dependem de setores de 512 bytes

Alguns aplicativos com formatos de arquivo padrão (como VHD 1,0) podem ter esses arquivos embutidos em código para assumir um tamanho de setor de 512 bytes. Assim, as atualizações e gravações nesse arquivo resultarão em um ciclo de leitura-modificação/gravação no dispositivo, o que potencialmente resultará em problemas de desempenho e resiliência para seus clientes. No entanto, há maneiras de um aplicativo fornecer suporte para operar nesse tipo de mídia, por exemplo:

-   Usar o buffer para garantir que as gravações sejam executadas em unidades do tamanho do setor físico
-   Implemente uma leitura-modificação-gravação interna que possa ajudar a garantir que as atualizações sejam executadas em unidades do tamanho do setor físico relatado
-   Se possível, preencha os registros para um setor físico, de forma que o preenchimento seja interpretado como espaço vazio
-   Considere reformular uma nova versão da estrutura de dados do aplicativo com suporte para setores maiores

### <a name="issue-4-the-reported-physical-sector-size-can-change-between-sessions"></a>Problema 4: o tamanho do setor físico relatado pode mudar entre sessões

Há muitos cenários em que o tamanho do setor físico relatado do armazenamento subjacente que hospeda o Datastor pode ser alterado. O mais comum deles é quando você migra o Datastor para outro volume, ou até mesmo pela rede. Uma alteração no tamanho do setor físico relatado pode ser um evento inesperado para muitos aplicativos e pode potencialmente resultar em alguns aplicativos que sequer falham ao reinicializar.

Esse não é o cenário mais fácil para oferecer suporte e é mencionado aqui como um comunicado. Você deve considerar os requisitos de mobilidade de seus clientes e ajustar seu suporte de forma adequada para ajudar a garantir que os clientes não sejam afetados negativamente usando a mídia 512e.

## <a name="4-kb-native-media"></a>Mídia nativa de 4 KB

a mídia de emulação de 512 bytes é destinada como uma etapa de transição entre a mídia nativa de 512 bytes e de 4 KB, e esperamos ver a mídia nativa de 4 KB lançada logo depois que 512e estiver disponível. Há várias implicações importantes nessa mídia que devem ser observadas:

-   Os tamanhos de setor lógico e físico são ambos 4 KB
-   Como não há nenhuma camada de emulação, as gravações não alinhadas serão reprovadas pelo armazenamento
-   Nenhuma queda de resiliência oculta – os aplicativos funcionam ou não funcionam

Embora a Microsoft esteja investigando o suporte para esses tipos de mídia em uma versão futura do Windows e emitirá um artigo da base de conhecimento quando apropriado, os desenvolvedores de aplicativos devem considerar o suporte preventivo para esses tipos de mídia.

## <a name="closing"></a>Fechamento

Neste artigo, discutimos os efeitos que a mídia de setor grande apresenta com muitos cenários de implantação comuns. Vimos o impacto de desempenho e resiliência de Read-Modify-Write, alguns dos cenários interessantes que essa mídia pode introduzir e o conjunto de problemas que eles podem causar potencialmente com software, o que, por fim, afeta o usuário final. O setor de armazenamento está fazendo uma transição rápida para a mídia com tamanhos de setor maiores, e os clientes muito logo não poderão comprar discos com tamanhos de setor de 512 bytes tradicionais.

Este é um documento dinâmico e se destina a ajudar os desenvolvedores a entender essa transição. Você deve iniciar uma conversa com suas respectivas organizações, com clientes, profissionais de ti e seus fornecedores de hardware para falar sobre a transição de setor grande e como ele afeta os cenários que são importantes para você.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   **Instrução de suporte geral do Windows**: <https://support.microsoft.com/kb/2510009>
-   **Hotfix para Windows 7 e Windows Server 2008 R2**: <https://support.microsoft.com/kb/982018>
-   **Hotfix para Windows Vista e Windows Server 2008**: <https://support.microsoft.com/kb/2470478>
-   **Instrução de suporte do HyperV**: <https://support.microsoft.com/kb/2515143>
-   **Informações gerais sobre o IOCTL \_ \_Código de \_ controle da propriedade de consulta de armazenamento**: [https://msdn.microsoft.com/library/ff560590.aspx](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   **IOCTL \_ \_Código de \_ controle da propriedade de consulta de armazenamento**: [https://msdn.microsoft.com/library/ff800830.aspx](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   **Informações gerais sobre o armazenamento \_ \_Estrutura do \_ descritor de alinhamento de acesso**: [https://msdn.microsoft.com/library/ff566344.aspx](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   **Descrição da terminologia padrão usada para descrever as atualizações de software da Microsoft**: <https://support.microsoft.com/kb/824684/>
-   **Código de exemplo do WDK** com detalhes sobre como extrair as informações de alinhamento de acesso de armazenamento relatado da estrutura do **\_ \_ \_ descritor de alinhamento de acesso de armazenamento** ao fazer uma chamada para o código de controle da **\_ \_ \_ propriedade de consulta de armazenamento do IOCTL** : [/Windows/Desktop/API/winioctl/NS-winioctl-storage_access_alignment_descriptor](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   **Informações gerais sobre as opções do ImageX Command-Line**: <https://technet.microsoft.com/library/dd799302(WS.10).aspx>
-   **Requisitos de driver de chipset Intel para dar suporte a unidades de setor de 4 KB**: <https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm>
-   Para obter mais informações sobre discos de formato avançado, visite os seguintes sites do IDEMA:
    -   <http://idema.org/?page_id=2172>
    -   <http://idema.org/?download=7926>

 

 
