---
description: Para reproduzir o pacote de patch de exemplo, você precisa de uma ferramenta de software capaz de criar e editar um pacote de patches Windows Installer.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Criando um arquivo de propriedades de criação de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769324"
---
# <a name="creating-a-patch-creation-properties-file"></a>Criando um arquivo de propriedades de criação de patch

Para reproduzir o pacote de patch de exemplo, você precisa de uma ferramenta de software capaz de criar e editar um pacote de patches Windows Installer. Várias ferramentas de criação de pacotes de patches estão disponíveis de fornecedores de software independentes. O exemplo discutido nas seções a seguir usa um editor de banco de dados Windows Installer chamado Orca para criar um arquivo de propriedades de criação de patch (extensão. PCP). O arquivo. PCP pode ser usado com os utilitários [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) para gerar um pacote de patches Windows Installer (extensão. msp). O orca, Msimsp.exe e Patchwiz.dll são fornecidos nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Um arquivo de propriedades de criação de patch em branco, template. PCP, também é fornecido com o SDK. Faça uma cópia de template. PCP e renomeie essa cópia MNP2000. PCP. Use o Orca ou outro editor de banco de dados para inserir os itens a seguir na tabela Properties de MNP2000. PCP. A tabela de propriedades contém configurações globais para o pacote de patch.

[Tabela de propriedades](properties-table-patchwiz-dll-.md)



| Nome                               | Valor                                  |
|------------------------------------|----------------------------------------|
| AllowProductCodeMismatches         | 1                                      |
| AllowProductVersionMajorMismatches | 1                                      |
| ApiPatchingSymbolFlags             | 0x00000000                             |
| DontRemoveTempFolderWhenFinished   | 1                                      |
| IncludeWholeFilesOnly              | 0                                      |
| ListOfPatchGUIDsToReplace          |                                        |
| ListOfTargetProductCodes           | \*                                     |
| PatchGUID                          | {5406B219-A1AC-4BC4-8695-72292C8195AC} |
| PatchOutputPath                    | c: \\ output. msp                         |
| PatchSourceList                    | PatchSourceList                        |



 

Use o editor de banco de dados do para inserir os itens a seguir na tabela ImageFamilies de MNP2000. PCP. A tabela ImageFamilies contém informações a serem adicionadas à [tabela de mídia](media-table.md) durante a aplicação de patch.

[Tabela ImageFamilies](imagefamilies-table-patchwiz-dll-.md)



| Família  | MediaSrcPropName | MediaDiskId | FileSequenceStart | DiskPrompt | VolumeLabel |
|---------|------------------|-------------|-------------------|------------|-------------|
| MNPapps | MNPSrcPropName   | 2           | 1000              |            |             |



 

Insira os dados a seguir na tabela UpgradedImages de MNP2000. PCP. A tabela UpgradedImages contém informações sobre a imagem atualizada que você criou no [planejamento de um patch de atualização pequeno](planning-a-small-update-patch.md).

[Tabela UpgradedImages](upgradedimages-table-patchwiz-dll-.md)



| Atualizado   | MsiPath                                           | PatchMsiPath | SymbolPaths | Família  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| MNP \_ fixo | C: \\ Observação \_ patch do instalador \\ \\ atualizado \\MNP2000.msi |              |             | MNPapps |



 

Insira os dados a seguir na tabela TargetImages de MNP2000. PCP. A tabela TargetImages contém informações sobre a imagem de destino.

[Tabela TargetImages](targetimages-table-patchwiz-dll-.md)



| Destino     | MsiPath                                         | SymbolPaths | Atualizado   | Ordem | ProductValidateFlags | IgnoreMissingSrcFiles |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| Erro de MNP \_ | C: \\ Observação \_ destino do patch do instalador \\ \\ \\MNP2000.msi |             | MNP \_ fixo | 1     |                      | 0                     |



 

Para o pacote de patch de exemplo, deixe as tabelas a seguir em MNP2000. PCP em branco.

[\_Tabela UpgradedFiles OptionalData](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[Tabela FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md)

[\_Tabela TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md)

[Tabela ExternalFiles](externalfiles-table-patchwiz-dll-.md)

[Tabela UpgradedFilesToIgnore](upgradedfilestoignore-table-patchwiz-dll-.md)

[Continuar](generating-a-patch-package.md)

 

 



