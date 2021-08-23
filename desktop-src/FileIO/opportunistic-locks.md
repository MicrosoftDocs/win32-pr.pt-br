---
description: Um bloqueio oportunista (também chamado de oplock) é um bloqueio colocado por um cliente em um arquivo que reside em um servidor.
ms.assetid: b4c2f5f0-a29b-4598-a49b-da99e93d2991
title: Bloqueios oportunistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89d3e984c5a8a1a1dc9cc1cb0c0c56e92434433b334747e832ea7f3bdf62d3da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683396"
---
# <a name="opportunistic-locks"></a>Bloqueios oportunistas

Um bloqueio oportunista (também chamado de oplock) é um bloqueio colocado por um cliente em um arquivo que reside em um servidor. Na maioria dos casos, um cliente solicita um bloqueio oportunista para que possa armazenar dados localmente em cache, reduzindo assim o tráfego de rede e melhorando o tempo de resposta aparente. Os bloqueios oportunistas são usados por redirecionadores de rede em clientes com servidores remotos, bem como por aplicativos cliente em servidores locais.

Os bloqueios oportunistas coordenam o cache de dados e a coerência entre clientes e servidores e entre vários clientes. Os dados que são coerentes são dados que são os mesmos na rede. Em outras palavras, se os dados forem coerentes, os dados no servidor e todos os clientes serão sincronizados.

Os bloqueios oportunistas não são comandos pelo cliente para o servidor. Eles são solicitações do cliente para o servidor. Do ponto de vista do cliente, eles são oportunistas. Em outras palavras, o servidor concede esses bloqueios sempre que outros fatores tornam os bloqueios possíveis.

Quando um aplicativo local solicita acesso a um arquivo remoto, a implementação de bloqueios oportunistas é transparente para o aplicativo. O redirecionador de rede e o servidor envolvidos abrem e fecham os bloqueios oportunistas automaticamente. No entanto, os bloqueios oportunistas também podem ser usados quando um aplicativo local solicita acesso a um arquivo local e o acesso por outros aplicativos e processos deve ser delegado para evitar a corrupção do arquivo. Nesse caso, o aplicativo local solicita diretamente um bloqueio oportunista do sistema de arquivos local e armazena o arquivo em cache localmente. Quando usado dessa forma, o bloqueio oportunista é efetivamente um semáforo gerenciado pelo servidor local e é usado principalmente para fins de coerência de dados na notificação de acesso a arquivos e arquivos.

Antes de usar bloqueios oportunistas em seu aplicativo, você deve estar familiarizado com os modos de acesso e compartilhamento de arquivos descritos em [criando e abrindo arquivos](creating-and-opening-files.md).

O número máximo de bloqueios oportunistas simultâneos que você pode criar é limitado apenas pela quantidade de memória disponível.

Os aplicativos locais não devem tentar solicitar bloqueios oportunistas de servidores remotos. Um erro será retornado por [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) se for feita uma tentativa de fazer isso.

Os bloqueios oportunistas são de uso muito limitado para aplicativos. O único uso prático é testar um redirecionador de rede ou um manipulador de bloqueio oportunista de servidor. Normalmente, os sistemas de arquivos implementam o suporte a bloqueios oportunistas. Os aplicativos geralmente deixam o gerenciamento de bloqueios oportunista para os drivers do sistema de arquivos. Qualquer pessoa que esteja implementando um sistema de arquivos deve usar o [Kit IFS (sistema de arquivos instalável)](https://www.microsoft.com/whdc/devtools/ifskit/default.mspx). qualquer pessoa que esteja desenvolvendo um driver de dispositivo que não seja um sistema de arquivos instalável deve usar o [Windows driver Kit (WDK)](https://www.microsoft.com/?ref=go).

Os bloqueios oportunistas e as operações associadas são um superconjunto da porção de bloqueio oportunista do protocolo CIFS (Common Internet File System), um rascunho da Internet. O protocolo CIFS é uma versão aprimorada do protocolo SMB. Para obter mais informações, consulte [Microsoft SMB Protocol and CIFS Protocol Overview](microsoft-smb-protocol-and-cifs-protocol-overview.md). O rascunho da Internet do CIFS identifica explicitamente que uma implementação de CIFS pode implementar bloqueios oportunistas ao se recusar a concedê-los.

Os tópicos a seguir identificam bloqueios oportunistas.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                               | Descrição                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Caching local](local-caching.md)<br/>                                                                       | O *cache local* de dados é uma técnica usada para acelerar o acesso à rede para arquivos de dados. Ele envolve o armazenamento em cache de dados em clientes em vez de servidores, quando possível.<br/>                                                                                                                           |
| [Coerência de dados](data-coherency.md)<br/>                                                                     | Se os dados forem coerentes, os dados no servidor e todos os clientes serão sincronizados. Um tipo de sistema de software que fornece a coerência de dados é um sistema de controle de revisão (RCS).<br/>                                                                                                              |
| [Como solicitar um bloqueio oportunista](how-to-request-an-opportunistic-lock.md)<br/>                         | Os bloqueios oportunistas são solicitados abrindo primeiro um arquivo com permissões e sinalizadores apropriados para o aplicativo que abre o arquivo. Todos os arquivos para os quais os bloqueios oportunistas serão solicitados devem ser abertos para a operação sobreposta (assíncrona).<br/>                                |
| [Resposta do servidor para abrir solicitações em arquivos bloqueados](server-response-to-open-requests-on-locked-files.md)<br/> | Você pode minimizar o impacto que seu aplicativo tem em outros clientes e o impacto que eles têm em seu aplicativo concedendo o máximo de compartilhamento possível, solicitando o nível mínimo de acesso necessário e usando o bloqueio oportunista menos intrusivo adequado para seu aplicativo.<br/> |
| [Tipos de bloqueios oportunistas](types-of-opportunistic-locks.md)<br/>                                         | Descreve os bloqueios oportunistas de nível 1, nível 2, lote e filtro.<br/>                                                                                                                                                                                                                     |
| [Interrompendo bloqueios oportunistas](breaking-opportunistic-locks.md)<br/>                                         | Interromper um bloqueio oportunista é o processo de degradação do bloqueio que um cliente tem em um arquivo para que outro cliente possa abrir o arquivo, com ou sem um bloqueio oportunista.<br/>                                                                                                     |
| [Exemplos de bloqueio oportunista](opportunistic-lock-examples.md)<br/>                                           | Diagramas de exibições de tráfego de rede para um bloqueio oportunista de nível 1, um bloqueio oportunista em lote e um bloqueio oportunista de filtro.<br/>                                                                                                                                                       |
| [Operações de bloqueio oportunista](opportunistic-lock-operations.md)<br/>                                       | Se um aplicativo solicita bloqueios oportunistas, todos os arquivos para os quais ele solicita bloqueios devem ser abertos para entrada e saída sobrepostas (assíncronas) usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o sinalizador **\_ \_ sobreposto do sinalizador de arquivo** .<br/>                                   |



 

Para obter informações adicionais sobre bloqueios oportunistas, consulte o documento de rascunho da Internet do CIFS. As discrepâncias entre este tópico e o rascunho de Internet atual do CIFS devem ser resolvidas em favor do rascunho da Internet do CIFS.

 

