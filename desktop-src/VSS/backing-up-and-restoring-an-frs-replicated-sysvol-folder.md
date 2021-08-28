---
description: Este tópico explica como determinar se uma pasta SYSVOL é replicada pelo DFSR ou FSR e explica como fazer backup e restaurar uma pasta SYSVOL replicada pelo FRS.
ms.assetid: 32d8a5bd-eeb4-4db6-8129-b5cd3508a7e5
title: Fazendo backup e restaurando uma pasta FRS-Replicated SYSVOL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d841f64bab62114824847f91876ba8bbffbb0166db942c0f3cb9d010b72f106
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124596"
---
# <a name="backing-up-and-restoring-an-frs-replicated-sysvol-folder"></a>Fazendo backup e restaurando uma pasta FRS-Replicated SYSVOL

A pasta de volume do sistema (SYSVOL) fornece um local padrão para armazenar elementos importantes de objetos e scripts do [política de grupo](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)) . Uma cópia da pasta SYSVOL existe em cada controlador de domínio em um domínio. A pasta SYSVOL é replicada pelo [DFSR (replicação sistema de arquivos distribuído)](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) ou pelo [FRS (serviço de replicação de arquivo)](/previous-versions/windows/it-pro/windows-server-2003/cc781582(v=ws.10)). Este tópico explica como determinar se uma pasta SYSVOL é replicada pelo DFSR ou FSR e explica como fazer backup e restaurar uma pasta SYSVOL replicada pelo FRS.

O FRS pode copiar o conteúdo do SYSVOL para outros controladores de domínio no domínio. O FRS monitora a pasta SYSVOL e, se ocorrer uma alteração em qualquer arquivo armazenado na pasta SYSVOL, o FRS replica automaticamente o arquivo alterado para as pastas SYSVOL nos outros controladores de domínio no domínio.

> [!Note]  
> Somente o modelo de Política de Grupo é replicado replicando o conteúdo da pasta SYSVOL. O contêiner de Política de Grupo é replicado por meio da replicação Active Directory. Para que Política de Grupo operem com êxito, o modelo de Política de Grupo e o contêiner de Política de Grupo devem estar disponíveis em um controlador de domínio.

 

Este tópico aborda os seguintes assuntos:

-   [Determinando se a pasta SYSVOL do controlador de domínio é replicada pelo DFSR ou pelo FRS](#determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs)
-   [Fazendo backup de uma pasta DFSR-Replicated SYSVOL](#backing-up-a-dfsr-replicated-sysvol-folder)
-   [fazendo backup de uma pasta FRS-Replicated SYSVOL em um domínio Windows server 2008 ou Windows server 2003](#backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain)
-   [Documento de metadados do gravador do FRS de exemplo](#sample-frs-writer-metadata-document)
-   [Definindo chaves do registro para uma restauração de uma pasta FRS-Replicated SYSVOL](#setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder)
-   [Executando uma restauração não autoritativa de uma pasta FRS-Replicated SYSVOL](#performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder)
-   [Executando uma restauração autoritativa de uma pasta FRS-Replicated SYSVOL](#performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder)

## <a name="determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs"></a>Determinando se a pasta SYSVOL do controlador de domínio é replicada pelo DFSR ou pelo FRS

A tabela a seguir resume como determinar se uma pasta SYSVOL do controlador de domínio está sendo replicada pelo [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) ou pelo FRS.

| Se o controlador de domínio estiver em execução                                                                                                                  | O SYSVOL é replicado por |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| Windows servidor 2008 + nível funcional de domínio do Windows server 2008 + [migração de SYSVOL](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) concluída | DFSR                    |
| Windows servidor 2008 + nível funcional de domínio abaixo Windows Server 2008                                                                              | DUPLIQUE                     |
| Windows Server 2003                                                                                                                                  | DUPLIQUE                     |



 

se o [nível funcional](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) do domínio for Windows Server 2008 e o domínio tiver passou na [migração de sysvol](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx), o [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) será usado para replicar a pasta sysvol. se o primeiro controlador de domínio no domínio tiver sido promovido diretamente para o [nível funcional](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))do Windows Server 2008, o DFSR será usado automaticamente para replicação do SYSVOL. Nesses casos, não há necessidade de migração de replicação de SYSVOL do FRS para o DFSR. se o domínio tiver sido atualizado para o [nível funcional](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))do Windows Server 2008, o frs será usado para replicação do SYSVOL até que o processo de [migração](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) do frs para o DFSR seja concluído.

para determinar se o DFSR ou o FRS está sendo usado em um controlador de domínio que está executando o Windows Server 2008, verifique o valor de **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** \\ **parameters** do sistema de domínios de \\ **migração sysvols** \\  \\  . Se essa subchave do registro existir e seu valor for definido como 3 (ELIMINAdo), o [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) estará sendo usado. Se a subchave não existir ou se tiver um valor diferente, o FRS será usado.

## <a name="backing-up-a-dfsr-replicated-sysvol-folder"></a>Fazendo backup de uma pasta DFSR-Replicated SYSVOL

Se a pasta SYSVOL for replicada pelo [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr), o gravador VSS do DFSR poderá ser usado para fazer o backup. Para obter mais informações sobre o gravador VSS DFSR, consulte [pastas replicadas do DFSR](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders).

## <a name="backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain"></a>fazendo backup de uma pasta FRS-Replicated SYSVOL em um domínio Windows server 2008 ou Windows server 2003

em um controlador de domínio que está executando o Windows server 2008 ou Windows server 2003, a infraestrutura do vss está presente e, portanto, o gravador VSS do frs pode ser usado para fazer backup da pasta SYSVOL e dos componentes do frs.

O documento de metadados do gravador do gravador VSS do FRS fornece informações sobre o local da pasta SYSVOL e as listas de exclusão para o gravador. Com base nessas informações, um aplicativo de backup VSS (solicitante) pode fazer backup da pasta SYSVOL usando as técnicas regulares de backup baseado em VSS.

O documento de metadados do gravador contém informações sobre o gravador, os dados que o gravador possui e como restaurá-los. Este é um documento somente leitura que pode ser recuperado pelo aplicativo de backup antes de fazer um backup. A ferramenta [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) pode ser usada para exibir o documento de metadados do gravador do gravador VSS do FRS. O comando [DiskShadow list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) fornece informações sobre os gravadores presentes no sistema. Essa lista contém informações sobre o gravador do FRS em controladores de domínio que usam o FRS para replicação do SYSVOL ou em servidores de arquivos que usam o FRS para replicação de [destinos de link DFS](/previous-versions/windows/it-pro/windows-server-2003/cc782417(v=ws.10)).

a seção exemplo de documento de metadados do gravador do frs a seguir mostra um exemplo de documento de metadados do gravador do frs para um controlador de domínio que tem a pasta sysvol em D: \\ Windows \\ SYSVOL. O caminho mostrado na seção "arquivos excluídos" será o mesmo obtido ao consultar a chave do registro **SYSVOL** do serviço Netlogon:

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **Netlogon** \\ **parâmetros** \\ **SYSVOL**

A única exceção a essa regra ocorre quando o controlador de domínio está no estado Redirecionado da [migração de SYSVOL](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx). Nesse estado, os gravadores correspondentes ao FRS e ao serviço [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) relatam suas respectivas cópias da pasta SYSVOL. No entanto, a cópia da pasta SYSVOL do serviço [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) (geralmente uma pasta chamada SYSVOL \_ DFSR) é a que é compartilhada pelo controlador de domínio; esse caminho é o que é referenciado pela chave do registro do **SYSVOL** .

O gravador VSS do FRS requer um método de restauração personalizado. Isso significa que determinadas etapas personalizadas devem ser executadas durante a restauração de arquivos que estão sendo replicados pelo FRS. Para obter mais informações, consulte executando uma restauração não autoritativa de uma pasta FRS-Replicated SYSVOL.

> [!Note]  
> os backups de estado do sistema para Windows controladores de domínio não incluem o banco de dados do frs que mantém informações de estado para o serviço FRS pertencentes aos arquivos dentro da pasta SYSVOL e outros conjuntos de conteúdo. O banco de dados do FRS, os logs de depuração, os arquivos da área de preparação e os arquivos na [pasta de dado pré-existente](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) são excluídos de um backup de estado do sistema. A especificação de gravador do FRS de exemplo a seguir contém a lista de exclusões na seção "arquivos excluídos".

 

## <a name="sample-frs-writer-metadata-document"></a>Documento de metadados do gravador do FRS de exemplo

veja a seguir um exemplo de documento de metadados do gravador do FRS para um controlador de domínio cujo caminho de pasta SYSVOL é D: \\ Windows \\ SYSVOL.

``` syntax
* WRITER "FRS Writer"
    - Writer ID   = {d76f5a28-3092-4589-ba48-2958fb88ce29}
    - Writer Instance ID = {07ae58e5-6977-4e34-9dfe-399bbd2cbe40}
    - Supports restore events = FALSE
    - Writer restore conditions = VSS_WRE_NEVER
    - Restore method = VSS_RME_CUSTOM
    - Requires reboot after restore = FALSE

    - Excluded files:
       - Exclude: Path = d:\windows\ntfrs\jet, Filespec = *
       - Exclude: Path = d:\Windows\debug\NtFrs, Filespec = NtFrs*
       - Exclude: Path = d:\windows\sysvol\domain\DO_NOT_REMOVE_NtFrs_PreInstall_Directory, Filespec = *
       - Exclude: Path = d:\windows\sysvol\domain\NtFrs_PreExisting___See_EventLog, Filespec = *
       - Exclude: Path = d:\windows\sysvol\staging\domain, Filespec = NTFRS_*

    - Component "FRS Writer:\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b"
       - Name: 'da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Logical Path: 'SYSVOL'
       - Full Path: '\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Caption: ''
       - Type: VSS_CT_FILEGROUP [2]
       - Is Selectable: 'TRUE'
       - Is top level: 'TRUE'
       - Notify on backup complete: 'TRUE'
       - Components:
       - File List: Path = d:\windows\sysvol, Filespec = *
       - Affected paths by this component:
         - d:\windows\sysvol
       - Affected volumes by this component:
         - \\?\Volume{da897ba5-5840-11db-93c1-806e6f6e6963}\ [D:\]
       - Component Dependencies:
```

## <a name="setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder"></a>Definindo chaves do registro para uma restauração de uma pasta FRS-Replicated SYSVOL

A chave do registro **BurFlags** é usada para executar Restaurações autoritativas ou não autoritativa em membros do FRS de conjuntos de réplicas DFS ou SYSVOL. A chave de registro global (computador-todo) **BurFlags** contém \_ valores reg DWORD e está localizada no seguinte local no registro:

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **NTFRS** \\ **parâmetros** \\ de **backup/restauração** \\ **na inicialização**

Os valores mais comuns para a chave do registro **BurFlags** são:

-   D2, também conhecido como restauração de modo não autoritativo.
-   D4, também conhecido como restauração de modo autoritativo.

Existem chaves de registro **BurFlags** globais e de conjunto de réplicas específicas. Definir a chave do registro global **BurFlags** reinicializa todos os conjuntos de réplicas que o membro mantém. Essa chave global deve ser definida quando o servidor mantém apenas um conjunto de réplicas ou quando os conjuntos de réplicas que ele contém são relativamente poucos em número e pequeno tamanho. Por exemplo, se o servidor for um controlador de domínio que não hospeda conjuntos de conteúdo replicados usando o FRS diferente da pasta SYSVOL, a chave do registro global **BurFlags** poderá ser definida.

A chave do registro global **BurFlags** é encontrada no seguinte local no registro:

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **NTFRS** \\ **parâmetros** \\ de **backup/restauração** \\ **na inicialização**

Ao contrário da chave global **BurFlags** , a chave **BurFlags** específica do conjunto de réplicas permite a reinicialização de conjuntos de réplicas individuais e discretos, permitindo que os conjuntos de replicação íntegros sejam deixados intactos.

As chaves do registro **BurFlags** específicas do conjunto de réplicas podem ser localizadas determinando o GUID desse conjunto de réplicas específico.

O procedimento a seguir descreve como determinar qual GUID corresponde a um determinado conjunto de réplicas e descreve como configurar uma restauração.

**Para determinar qual GUID corresponde a um determinado conjunto de réplicas e configurar uma restauração**

1.  Pare o serviço FRS.
2.  Para determinar o GUID que representa um determinado conjunto de réplicas:
    1.  Localize a chave a seguir no registro.

        **HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **NTFRS** \\  \\ **conjuntos de réplicas**

    2.  Abaixo da subchave **conjuntos de réplicas** , há uma ou mais subchaves que são identificadas por um GUID.
    3.  O valor **raiz do conjunto de réplicas** para cada GUID é um caminho do sistema de arquivos que indica o conjunto de réplicas representado por esse GUID.
    4.  Itere sobre esta lista de GUIDs até que o conjunto de réplicas desejado esteja localizado. Observe o GUID correspondente.

3.  Localize a seguinte subchave no registro:

    **HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **NTFRS** \\  \\ **conjuntos de réplicas cumulativas**

4.  Abaixo dessa subchave, localize o mesmo GUID que foi anotado na etapa 2. Abaixo da subchave GUID, crie uma entrada para a chave **BurFlags** .
5.  Reinicie o serviço FRS.

## <a name="performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Executando uma restauração não autoritativa de uma pasta FRS-Replicated SYSVOL

A restauração não autoritativa é a maneira mais comum de reinicializar a replicação do SYSVOL em controladores de domínio individuais. Os controladores de domínio que são restaurados de forma não autoritativa devem ter conexões de entrada de outros controladores de domínio de trabalho, que participam do Active Directory e da replicação FRS. Em um ambiente de implantação grande que consiste em muitos controladores de domínio, os controladores de domínio restantes podem ser recuperados usando uma restauração de modo não autoritativo sob as seguintes condições:

-   Deve haver pelo menos um membro de réplica válido conhecido (um controlador de domínio com uma pasta SYSVOL íntegra).
-   Os outros controladores de domínio devem ser reinicializados na ordem do parceiro de replicação direta.

O procedimento a seguir descreve como executar uma restauração não autoritativa.

**Para executar uma restauração não autoritativa**

1.  Pare o serviço FRS.
2.  Restaure os dados de backup para a pasta SYSVOL.
3.  Configure a chave do registro **BurFlags** definindo o valor da seguinte chave do registro para o valor DWORD D2.

    **HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **NTFRS** \\ **parâmetros** \\ de **backup/restauração** \\ **no BurFlags de inicialização** \\ 

4.  Reinicie o serviço FRS.

Quando o serviço FRS é reiniciado, ocorrem as seguintes ações:

-   O valor da chave do registro **BurFlags** é redefinido como zero.
-   Os arquivos nas pastas FRS reinicializadas são movidos para uma pasta pré-existente.
-   O evento 13565 é registrado no log de eventos do FRS para sinalizar que uma restauração não autoritativa foi iniciada.
    > [!Note]  
    > Os códigos de evento do FRS são documentados em "códigos de erro do log de eventos do FRS" na base de dados de conhecimento de ajuda e suporte em <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

-   O banco de dados do FRS é recriado.
-   O membro executa uma junção inicial do conjunto de réplicas de um parceiro upstream ou do computador especificado na chave do registro **pai do conjunto de réplicas** se um pai tiver sido especificado para conjuntos de réplicas do SYSVOL.
-   O computador reinicializado executa uma replicação completa dos conjuntos de réplicas afetados quando o agendamento de replicação relevante é iniciado.
-   Quando o processo for concluído, um evento 13516 será registrado para sinalizar que o FRS está operacional. Se o evento não estiver registrado, haverá um problema com a configuração do FRS.

> [!Note]  
> O posicionamento de arquivos na pasta [pré-existente](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) em Membros reinicializados é uma proteção no FRS que foi projetada para evitar a perda acidental de dados. Todos os arquivos destinados à réplica que existem somente na pasta local pré-existente e que foram replicados após a replicação inicial podem ser copiados para a pasta apropriada. Quando a replicação de saída ocorre, os arquivos na pasta pré-existente podem ser excluídos para liberar espaço adicional na unidade.

 

## <a name="performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Executando uma restauração autoritativa de uma pasta FRS-Replicated SYSVOL

As restaurações autorizadas são usadas como um último recurso no caso de situações críticas, como divergência de dados no conjunto de conteúdo causado por colisões de diretório. Por exemplo, uma restauração autoritativa pode ser necessária para restaurar um conjunto de réplicas FRS em que a replicação foi interrompida completamente e uma recompilação do zero é necessária.

Se você precisar executar uma restauração autoritativa da pasta SYSVOL, lembre-se de que é um processo muito complicado. Diretrizes abrangentes detalhando as operações que precisam ser executadas para uma restauração autoritativa do conteúdo da pasta SYSVOL estão documentadas em "como recriar a árvore SYSVOL e seu conteúdo em um domínio" na base de dados de conhecimento de ajuda e suporte em <https://go.microsoft.com/fwlink/p/?linkid=117780> .

Os requisitos a seguir devem ser atendidos antes da execução de uma restauração autoritativa do FRS:

1.  O serviço FRS deve ser desabilitado em todos os parceiros de replicação downstream (direto e transitiva) para a pasta SYSVOL reinicializada antes que a restauração autoritativa tenha sido configurada para ocorrer.
2.  Os eventos 13553 e 13516 foram registrados no log de eventos do FRS. Esses eventos indicam que a associação do conjunto de réplicas do SYSVOL foi estabelecida no controlador de domínio configurado para a restauração autoritativa.
    > [!Note]  
    > Os códigos de evento do FRS são documentados em "códigos de erro do log de eventos do FRS" na base de dados de conhecimento de ajuda e suporte em <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

3.  O controlador de domínio configurado para a restauração autoritativa é configurado para ser autoritativo para todos os dados do SYSVOL que serão replicados para os controladores de domínio restantes.
4.  Todos os outros parceiros no conjunto de réplicas devem ser reinicializados com uma restauração não autoritativa.

 

 
