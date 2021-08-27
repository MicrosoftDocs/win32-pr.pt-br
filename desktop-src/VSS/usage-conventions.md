---
description: Ao desenvolver seu próprio aplicativo VSS, você deve observar as diretrizes e restrições a seguir.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Compatibilidade do aplicativo VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca1f6f3013856087e70247aed21d8f35aa4cf09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483012"
---
# <a name="vss-application-compatibility"></a>Compatibilidade do aplicativo VSS

Ao desenvolver seu próprio aplicativo VSS, você deve observar as diretrizes e restrições a seguir. talvez você ache útil consultar o código de exemplo para solicitantes, provedores e gravadores do VSS fornecidos no SDK (Software Development Kit) do Microsoft Windows.

> [!Note]  
> o SDK do Windows pode ser usado para desenvolver aplicativos VSS somente para Windows Vista e versões posteriores do sistema operacional Windows. ele não pode ser usado para desenvolver solicitantes, provedores ou gravadores VSS para Windows server 2003 R2, Windows Server 2003 ou Windows XP.

 

**Windows server 2003 R2, Windows server 2003 e Windows XP:** O VSS está disponível no SDK do Serviço de Cópias de Sombra de Volume 7,2, do qual você pode baixar [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) . observe que os arquivos vssapi. lib de 64 bits nos diretórios no diretório do Win2003 \\ Obj podem ser usados para as versões de 64 bits do Windows Server 2003 R2, Windows Server 2003 e Windows XP. Esse SDK também fornece código de exemplo para solicitantes, provedores e gravadores do VSS.

## <a name="compiling-vss-applications"></a>Compilando aplicativos VSS

Ao desenvolver um solicitante, como um aplicativo de backup:

-   Inclua os seguintes cabeçalhos: <dl> VSS. h  
    VsWriter. h  
    VsBackup. h  
    </dl>
-   Link the following library: <dl> VssApi. lib  
    </dl>

Ao desenvolver um gravador:

-   Inclua os seguintes cabeçalhos: <dl> VSS. h  
    VsWriter. h  
    </dl>
-   Link the following library: <dl> VssApi. lib  
    </dl>

## <a name="supported-configurations-and-restrictions"></a>Configurações e restrições com suporte

A lista a seguir descreve as configurações e restrições com suporte:

-   o VSS é fornecido e tem suporte em versões do sistema operacional Windows a partir do Windows XP.
-   a tabela a seguir resume as informações de compatibilidade entre Windows versões. observe que, se um aplicativo VSS for "compilado para" uma versão especificada do Windows, isso significará que o aplicativo foi compilado usando os arquivos de cabeçalho e as bibliotecas específicas dessa versão.

    > [!Note]  
    > os provedores de Hardware serão executados somente em versões do sistema operacional Windows server. eles não serão executados no Windows versões do sistema operacional do cliente.

     

    > [!Note]  
    > nas tabelas a seguir, Windows server 2008 com Service Pack 2 (SP2) deve ser considerado o mesmo que Windows Server 2008. para obter mais informações sobre o Windows Server 2008 com SP2, consulte <https://go.microsoft.com/fwlink/p/?linkid=178730> . Windows o servidor 2003 R2 deve ser considerado o mesmo que o Windows Server 2003.

     

    > [!Note]  
    > se um aplicativo VSS for compilado para o Windows Server 2003 ou posterior, ele também será executado em versões posteriores do Windows.

     

    

    
| Solicitantes, gravadores e provedores do VSS compilados para | Será executado em | 
|-----------------------------------------------------|-------------|
| Windows server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) e Windows Vista (64 bits) | Windows server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) e Windows Vista (64 bits) | 
| Windows server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) e Windows Vista (32 bits) | Windows server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) e Windows Vista (32 bits) | 
| Windows Server 2003 (64 bits) | Windows server 2008 R2 (64 bits), Windows 7 (64 bits), Windows server 2008 (64 bits), Windows Vista (64 bits) e Windows server 2003 (64 bits) | 
| Windows Server 2003 (32 bits) | Windows server 2008 R2 (32 bits), Windows 7 (32 bits), Windows server 2008 (32 bits), Windows Vista (32 bits) e Windows server 2003 (32 bits)    <blockquote>    [!Note]<br />    os solicitantes também serão executados no Windows Server 2003 (64 bits).    </blockquote><br /> | 
| Windows XP 64-edição de bits | Windows Server 2003 (64 bits) e Windows XP 64-bit Edition | 
| Windows XP (32 bits) | Windows XP (32 bits) | 


    

     

    

    | Para compilar um solicitante, gravador ou provedor do VSS para        | Use                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows Server 2008 R2 ou Windows 7                        | Windows SDK para Windows 7 (disponível no [centro de Download de Windows](https://www.microsoft.com/download/details.aspx?id=8279)).                |
    | Windows Server 2008 ou Windows Vista                       | Windows SDK para o Windows Server 2008 (disponível no [SDK do Windows developer Center](https://msdn.microsoft.com/windows/bb980924.aspx)). |
    | Windows server 2003 R2, Windows Server 2003 ou Windows XP | [SDK do Serviço de Cópias de Sombra de Volume 7,2](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   Todos os aplicativos VSS de 32 bits (solicitantes, provedores e gravadores) devem ser executados como aplicativos nativos de 32 bits ou de 64 bits. Não há suporte para executá-los em WOW64.

    **Windows Server 2003 e Windows XP:** A execução de solicitantes do VSS de 32 bits no WOW64 tem suporte, mas não para backups de estado do sistema. Não há suporte para a execução de provedores VSS de 32 bits e gravadores no WOW64. o suporte para a execução de solicitantes de 32 bits no WOW64 foi removido no Windows Vista e em versões subsequentes.

-   uma cópia de sombra criada no Windows server 2003 R2 ou Windows server 2003 não pode ser usada em um computador que esteja executando o Windows server 2008 R2 ou Windows server 2008. uma cópia de sombra criada no Windows server 2008 R2 ou no Windows server 2008 não pode ser usada em um computador que esteja executando o Windows server 2003. no entanto, uma cópia de sombra criada no Windows Server 2008 pode ser usada em um computador que esteja executando o Windows server 2008 R2 e vice-versa.
-   Para dar suporte a cópias de sombra, um sistema executando o VSS deve ter pelo menos um sistema de arquivos NTFS. Esse sistema de arquivos hospedará a "área de comparação" da cópia de sombra. Para obter mais informações, consulte [provedor do sistema](providers.md).
-   Dada a presença de um sistema de arquivos NTFS e, considerando a opção apropriada de contexto (consulte [configurações de contexto de cópia de sombra](shadow-copy-context-configurations.md)), qualquer sistema de arquivos local com suporte pode ser copiado em sombra.
-   Você pode fazer cópias de sombra somente para sistemas de arquivos montados localmente. Compartilhamentos remotos e outros sistemas de arquivos com montagem cruzada não podem ser copiados em sombra pelo sistema que os monta. Esses sistemas de arquivos podem ser copiados em sombra somente pelos sistemas que servem os sistemas de arquivos.
-   Gravadores e solicitantes devem especificar apenas recursos locais. Os recursos locais são conjuntos de arquivos cujo caminho absoluto começa com uma letra da unidade e a letra da unidade não pode ser associada a uma pasta montada em um compartilhamento remoto.
-   O número máximo de cópias de sombra de software para cada volume é 512. No entanto, por padrão, você só pode manter 64 cópias de sombra usadas pelo recurso Cópias de Sombra de Pastas Compartilhadas. Para alterar o limite para as cópias de sombra do recurso de pastas compartilhadas, use a chave do registro [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) .
-   A infraestrutura de componentes de backup não dá suporte ao backup de recursos de cluster como componentes do gravador. Para fazer backup de recursos de cluster, os aplicativos devem assumir que o caminho é local para um nó de cluster específico especificado.
-   [!Note]  
    > a Microsoft não fornece suporte técnico de desenvolvedor ou profissional de ti para implementar restaurações de estado do sistema online em Windows (todas as versões).

     

    Durante o backup e a recuperação do estado do sistema, a estratégia recomendada é fazer backup e recuperar os volumes do sistema e de inicialização, além dos arquivos enumerados pelos gravadores do estado do sistema.

    > [!Note]  
    > Os gravadores de estado do sistema são gravadores que têm o atributo de [**\_ \_ tipo de uso do VSS**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) definido como VSS \_ UT \_ BOOTABLESYSTEMSTATE ou VSS \_ UT \_ SYSTEMSERVICE.

     

 

 
