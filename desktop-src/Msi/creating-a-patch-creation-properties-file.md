---
description: Para reproduzir o pacote de patch de exemplo, você precisa de uma ferramenta de software capaz de criar e editar um pacote de patch Windows instalador.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Criando um arquivo de propriedades de criação de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50873fd508aa9f31435bd401284d38d13310991e150b28f4e24e5ec27f505dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379401"
---
# <a name="creating-a-patch-creation-properties-file"></a>Criando um arquivo de propriedades de criação de patch

Para reproduzir o pacote de patch de exemplo, você precisa de uma ferramenta de software capaz de criar e editar um pacote de patch Windows instalador. Várias ferramentas de criação de pacote de patch estão disponíveis de fornecedores independentes de software. O exemplo discutido nas seções a seguir usa um editor de banco de dados Windows Installer chamado Orca para criar um arquivo de propriedades de criação de patch (extensão .pcp). O arquivo .pcp pode ser usado com os utilitários [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) para gerar um pacote de patch do instalador do Windows (extensão .msp). Orca, Msimsp.exe e Patchwiz.dll são fornecidos nos componentes do SDK do Windows para desenvolvedores do [Windows Installer.](platform-sdk-components-for-windows-installer-developers.md)

Um arquivo de propriedades de criação de patch em branco, template.pcp, também é fornecido com o SDK. Faça uma cópia de template.pcp e renomeie essa cópia MNP2000.pcp. Use Orca ou outro editor de banco de dados para inserir os dados a seguir na tabela Propriedades de MNP2000.pcp. A tabela Propriedades contém configurações globais para o pacote de patch.

[Tabela de Propriedades](properties-table-patchwiz-dll-.md)



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
| PatchOutputPath                    | c: \\ output.msp                         |
| PatchSourceList                    | PatchSourceList                        |



 

Use o editor de banco de dados para inserir os dados a seguir na tabela ImageFamilies de MNP2000.pcp. A tabela ImageFamilies contém informações a serem adicionadas à tabela [Mídia](media-table.md) durante a adoção de patch.

[Tabela ImageFamilies](imagefamilies-table-patchwiz-dll-.md)



| Família  | MediaSrcPropName | MediaDiskId | FileSequenceStart | DiskPrompt | VolumeLabel |
|---------|------------------|-------------|-------------------|------------|-------------|
| MNPapps | MNPSrcPropName   | 2           | 1000              |            |             |



 

Insira os dados a seguir na tabela UpgradedImages de MNP2000.pcp. A tabela UpgradedImages contém informações sobre a imagem atualizada que você criou em [Planejando um patch de atualização pequena.](planning-a-small-update-patch.md)

[Tabela UpgradedImages](upgradedimages-table-patchwiz-dll-.md)



| Atualizado   | MsiPath                                           | PatchMsiPath | SymbolPaths | Família  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| MNP \_ fixo | C: \\ Observação Atualização do patch do \_ \\ \\ \\ instaladorMNP2000.msi |              |             | MNPapps |



 

Insira os dados a seguir na tabela TargetImages de MNP2000.pcp. A tabela TargetImages contém informações sobre a imagem de destino.

[Tabela TargetImages](targetimages-table-patchwiz-dll-.md)



| Destino     | MsiPath                                         | SymbolPaths | Atualizado   | Ordem | ProductValidateFlags | IgnoreMissingSrcFiles |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| Erro de \_ MNP | C: Observação o \\ sistema de destino de patch do \_ \\ \\ \\ instaladorMNP2000.msi |             | MNP \_ fixo | 1     |                      | 0                     |



 

Para o pacote de patch de exemplo, deixe as tabelas a seguir em MNP2000.pcp em branco.

[Tabela UpgradedFiles \_ OptionalData](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[Tabela FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md)

[Tabela TargetFiles \_ OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md)

[Tabela ExternalFiles](externalfiles-table-patchwiz-dll-.md)

[Tabela UpgradedFilesToIgnore](upgradedfilestoignore-table-patchwiz-dll-.md)

[Continuar](generating-a-patch-package.md)

 

 



