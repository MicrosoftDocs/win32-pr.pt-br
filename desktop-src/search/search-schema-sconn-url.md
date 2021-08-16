---
description: O <url> elemento Especifica uma URL para o local para esse conector de pesquisa.
ms.assetid: fdc9e138-2e98-4f01-ab7b-0c3dfad5a4dd
title: Elemento URL simpleLocation (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce95943017f4905414f65b75086d4babdf3750505fece0b73255e0e63623e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226321"
---
# <a name="simplelocation-url-element-search-connector-schema"></a>Elemento URL simpleLocation (esquema do conector de pesquisa)

O <url> elemento Especifica uma URL para o local para esse conector de pesquisa. Esse valor pode ser uma URL file://regular, conforme definido no RFC 1738 ( https://www.ietf.org/rfc/rfc1738.txt) documento ou ou uma URL que usa o protocolo KnownFolders:. Este elemento não tem elementos filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- url element for simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                             | Elementos filho |
|--------------------------------------------------------------------------------------------|----------------|
| [Elemento simpleLocation (esquema do conector de pesquisa)](search-schema-sconn-simplelocation.md) |                |



 

## <a name="remarks"></a>Comentários

Consulte [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid) para obter uma lista de GUIDs de pasta conhecidos. Use o seguinte formato para o valor desse elemento ao usar o protocolo KnownFolder:.


```
<url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
```



a tabela a seguir mostra os guids de pasta conhecidos do Windows 7.



| Pasta conhecida                     | GUID                                         |
|----------------------------------|----------------------------------------------|
| PASTA de \_ AdminTools             | {724EF170-A42D-4FEF-9F-26-B6-0E-84-6F-BA-4F} |
| PASTA de \_ AppUpdates             | {a305ce99-f527-492b-8B-1a-7e-76-fa-98-D6-E4} |
| PASTA de \_ AddNewPrograms         | {de61d971-5ebc-4F02-a3-a9-6C-82-89-5E-5C-04} |
| PASTA de \_ CDBurning              | {9E52AB10-F80D-49DF-AC-B8-43 -30-F5-68-78-55} |
| PASTA de \_ ChangeRemovePrograms   | {df7266ac-9274-4867-8D-55-3B-D6-61-de-87-2D} |
| PASTA de \_ CommonAdminTools       | {D0384E7D-BAC3-4797-8F-14-CB-A2-29-B3-92-B5} |
| PASTA de \_ CommonOEMLinks         | {C1BAE2D0-10DF-4334-SER-DD-7A-A2-0B-22-7A-9D} |
| PASTA de \_ commonprograms         | {0139D44E-6AFE-49F2-86-90-3D-AF-CA-E6-FF-B8} |
| PASTA de \_ CommonStartMenu        | {A4115719-D62E-491D-AA-7C-E7-4B-8B-E3-B0-67} |
| PASTA de \_ CommonStartup          | {82A5EA35-D9CD-47C5-96 -29-E1-5D-2F-71-4E-6E} |
| PASTA de \_ CommonTemplates        | {B94237E7-57AC-4347-91-51-B0-8C-6C-32-D1-F7} |
| PASTA de \_ ComputerFolder         | {0AC0837C-BBF8-452A-85-0D-79-D0-8E-66-7C-A7} |
| PASTA de \_ ConflictFolder         | {4bfefb45-347d-4006-a5-is-AC-0c-B0-56-71-92} |
| PASTA de \_ ConnectionsFolder      | {6F0CD92B-2E97-45D1-88-FF-B0-D1-86-B8-DE-DD} |
| Contatos de FOLDERid \_               | {56784854-C6CB-462b-81-69-88-E3-50-AC-B8-82} |
| PASTA de \_ ControlPanelFolder     | {82A74AEB-AEB4-465C-A0-14-D0-97-EE-34-6D-63} |
| Cookies FOLDERid \_                | {2B0F765D-C0E9-4171-90-8E-08-A6-11-B8-4F-F6} |
| Área de \_ trabalho da pasta                | {B4BFCC3A-DB2C-424C-B0-29-7F-E9-9A-87-C6-41} |
| PASTA de \_ DeviceMetadataStore    | {5ce4a5e9-e4eb-479d-B8-9F-13-0c-02-88-61-55} |
| Documentos de FOLDERid \_              | {FDD39AD0-238F-46AF-AD-B4-6C-85-48-03-69-C7} |
| PASTA de \_ DocumentsLibrary       | {7b0db17d-9cd2-4a93-97-33 -46-CC-89-02-2e-7C} |
| Downloads de FOLDERid \_              | {374de290-123f-4565-91-64-39-C4-92-5E-46-7B} |
| Favoritos da PASTAid \_              | {1777F761-68AD-4D8A-87-BD-30-B7-59-FA-33-DD} |
| Fontes FOLDERid \_                  | {FD228CB7-AE11-4AE3-86-4C-16-F3-91-0A-B8-FE} |
| Jogos de PASTAid \_                  | {cac52c1a-b53d-4edc-92-D7-6B-2e-8a-C1-94-34} |
| PASTA de \_ GameTasks              | {54fae61-4dd8-4787 -80-B6-9-2 -20-C4-B7-0}     |
| Histórico de FOLDERid \_                | {D9DC8A3B-B784-432E-A7-81-5A-11-30-A7-59-63} |
| \_Grupo doméstico da pasta              | {52528a6b-b9e3-4Add-B6-d-58-8C-2D-BA-84-2D}  |
| PASTA de \_ ImplicitAppShortcuts   | {bcb5256f-79f6-4cee-B7-25-DC-34-E4-2-FD-46}  |
| PASTA de \_ InternetCache          | {352481E8-33BE-4251-BA-85-60-07-CA-ED-CF-9D} |
| PASTA de \_ InternetFolder         | {4D9F7874-4E0C-4904-96-7B-40-B0-D2-0C-3E-4B} |
| Bibliotecas FOLDERid \_              | {1b3ea5dc-b587-4786-B4-EF-BD-1D-C3-32-AE-AE} |
| Links de FOLDERid \_                  | {bfb9d5e0-c6a9-404c-B2-B2-AE-6D-B6-AF-49-68} |
| PASTA de \_ LocalAppData           | {F1B32785-6FBA-4FCF-9D-55-7B-8E-7F-15-70-91} |
| PASTA de \_ LocalAppDataLow        | {A520A1A4-1780-4FF6-BD-18-16-73-43-C5-AF-16} |
| PASTA de \_ LocalizedResourcesDir  | {2A00375E-224C-49DE-B8-D1-44-0D-F7-EF-3D-DC} |
| PASTA de \_ músicas                  | {4BD8D571-6D19-48D3-IS-97-42-22-20-08-0E-43} |
| PASTA de \_ MusicLibrary           | {2112ab0a-c86a-4FFE-a3-68-d-E9-6e-47-1-2e}   |
| PASTA de os \_ Netbastidores                | {C5ABBF53-E17F-4121-89-00-86-62-6F-C2-C9-73} |
| PASTA de \_ NetworkFolder          | {D20BEEC4-5CA8-4905-AE-3B-BF-25-1E-A0-9B-53} |
| PASTA de \_ OriginalImages         | {2C36C0AA-5812-4b87-BF-D0-4C-D0-DF-B1-9B-39} |
| Metaálbums de FOLDERid \_            | {69D2CF90-FC33-4FB7-9A-0C-EB-B0-F0-FC-B4-3C} |
| Imagens \_ FOLDERID               | {33E28130-4E1E-4676-83-5A-98-39-5C-3B-C3-BB} |
| FOLDERID \_ PicturesLibrary        | {a990ae9f-a03b-4e80-94-bc-99-12-d7-50-41-4}  |
| Listas de reprodução FOLDERID \_              | {DE92C1C7-837F-4F69-A3-BB-86-E6-31-20-4A-23} |
| FOLDERID \_ PrintersFolder         | {76FC4E2D-D6AD-4519-A6-63-37-BD-56-06-81-85} |
| FOLDERID \_ Print Projeto              | {9274BD8D-CFD1-41C3-B3-5E-B1-3F-55-A7-58-F4} |
| Perfil \_ FOLDERID                | {5E6C858F-0E22-4760-9A-FE-EA-33-17-B6-71-73} |
| FOLDERID \_ ProgramData            | {62AB5D82-FDC1-4DC3-A9-DD-07-0D-1D-49-5D-97} |
| FOLDERID \_ ProgramFilesX86        | {7C5A40EF-A0FB-4BFC-87-4A-C0-F2-E0-B9-FA-8E} |
| FOLDERID \_ ProgramFilesCommonX86  | {DE974D24-D9C6-4D3E-BF-91-F4-45-51-20-B9-17} |
| FOLDERID \_ ProgramFilesX64        | {6d809377-6af0-444b-89-57-a3-77-3f-02-20-0e} |
| FOLDERID \_ ProgramFilesCommonX64  | {6365d5a7-f0d-45e5-87-f6-d-a5-6b-6a-4f-7d}   |
| FOLDERID \_ ProgramFiles           | {905e63b6-c1bf-494e-b2-9c-65-b7-32-d3-d2-1a} |
| FOLDERID \_ ProgramFilesCommon     | {F7F1ED05-9F6D-47A2-AA-AE-29-D3-17-C6-F0-66} |
| Programas \_ FOLDERID               | {A77F5D77-2E2B-44C3-A6-A2-AB-A6-01-05-4A-51} |
| FOLDERID \_ Public                 | {DFDF76A2-C82A-4D63-90-6A-56-44-AC-45-73-85} |
| FOLDERID \_ PublicDesktop          | {C4AA340D-F20F-4863-AF-EF-F8-7E-F2-E6-BA-25} |
| FOLDERID \_ PublicDocuments        | {ED4824AF-DCE4-45A8-81-E2-FC-79-65-08-36-34} |
| FOLDERID \_ PublicDownloads        | {3d644c9b-1fb8-4f30-9b-45-f6-70-23-5f-79-c0} |
| FOLDERID \_ PublicGameTasks        | {debf2536-e1a8-4c59-b6-a2-41-45-86-47-6a-ea} |
| FOLDERID \_ PublicMusic            | {3214FAB5-9757-4298-BB-61-92-A9-DE-AA-44-FF} |
| FOLDERID \_ PublicPictures         | {B6EBFB86-6907-413C-9A-F7-4F-C2-AB-F0-7C-C5} |
| FOLDERID \_ PublicRbones        | {E555AB60-153B-4D17-9F-04-A5-FE-99-FC-15-EC} |
| FOLDERID \_ PublicVideos           | {2400183A-6185-49FB-A2-D8-4A-39-2A-60-2B-A3} |
| FOLDERID \_ QuickLaunch            | {52a4f021-7b75-48a9-9f-6b-4b-87-a2-10-bc-8f} |
| FOLDERID \_ Recente                 | {AE50C081-EBD2-438A-86-55-8A-09-2E-34-98-7A} |
| FOLDERID \_ RecordedTVLibrary      | {1a6fdba2-f42d-4358-a7-98-b7-4d-74-59-26-c5} |
| FOLDERID \_ RecycleBinFolder       | {B7534046-3ECB-4C18-BE-4E-64-CD-4C-B7-D6-AC} |
| FOLDERID \_ ResourceDir            | {8AD10C31-2ADB-4296-A8-F7-E4-70-12-32-C9-72} |
| Anéis FOLDERID \_              | {C870044B-F49E-4126-A9-C3-B5-2A-1F-F4-11-E8} |
| FOLDERID \_ RoamingAppData         | {3EB685DB-65F9-4CF6-A0-3A-E3-EF-65-72-9F-3D} |
| FOLDERID \_ SamplePlaylists        | {15CA69B3-30EE-49C1-AC-E1-6B-5E-C3-72-AF-B5} |
| FOLDERID \_ SampleMusic            | {B250C668-F57D-4EE1-A6-3C-29-0E-E7-D1-AA-1F} |
| FOLDERID \_ SamplePictures         | {C4900540-2379-4C75-84-4B-64-E6-FA-F8-71-6B} |
| FOLDERID \_ SampleVideos           | {859EAD94-2E85-48AD-A7-1A-09-69-CB-56-A6-CD} |
| FOLDERID \_ SavedGames             | {4c5c32ff-bb9d-43b0-b5-b4-2d-72-e5-4e-aa-a4} |
| FOLDERID \_ SavedSearches          | {7d1d3a04-debb-4115-95-cf-2f-29-da-29-20-da} |
| CSC DE \_ PESQUISA DE \_ FOLDERID            | {ee32e446-31ca-4aba-81-4f-a5-eb-d2-fd-6d-5e} |
| FOLDERID \_ SEARCH \_ MAPI           | {98ec0e18-2098-4d44-86-44-66-97-93-15-a2-81} |
| FOLDERID \_ SearchHome             | {190337d1-b8ca-4121-a6-39-6d-47-2d-16-97-2a} |
| FOLDERID \_ SendTo                 | {8983036C-27C0-404B-8F-08-10-2D-10-DC-FD-74} |
| FOLDERID \_ StartMenu              | {625B53C3-AB48-4EC1-BA-1F-A1-EF-41-46-FC-19} |
| Inicialização \_ de FOLDERID                | {B97D20BB-F46A-4C97-BA-10-5E-36-08-43-08-54} |
| FOLDERID \_ SyncManagerFolder      | {43668BF8-C14E-49B2-97-C9-74-77-84-D7-84-B7} |
| FOLDERID \_ SyncResultsFolder      | {289a9a43-be44-4057-a4-1b-58-7a-76-d7-e7-f9} |
| FOLDERID \_ SyncSetupFolder        | {f214138-b1d3-4a90-bb-a9-27-cb-c0-c5-38-9a}  |
| Sistema \_ FOLDERID                 | {1AC14E77-02E7-4E5D-B7-44-2E-B1-AE-51-98-B7} |
| FOLDERID \_ SystemX86              | {D65231B0-B2F1-4857-A4-CE-A8-E7-C6-EA-7D-27} |
| Modelos \_ FOLDERID              | {A63293E8-664E-48DB-A0-79-DF-75-9E-05-09-F7} |
| FOLDERID \_ UserPinned             | {9e3995ab-1f9c-4f13-b8-27-48-b2-4b-6c-71-74} |
| Usuários \_ FOLDERIDArquivos             | {f3ce0f7c-4901-4acc-86-48-D5-D4-4B-04-EF-8F} |
| PASTA de \_ UsersLibraries         | {a302545d-definitivamente-464b-AB-E8-61-C8-64-8D-93-9B} |
| PASTA de os perfis de user \_           | {0762D272-C50A-4BB0-A3-82-69-7D-CD-72-9B-80} |
| FOLDERid \_ Userprogramfiles       | {5cd7aee2-2219-4A67-B8-5D-6C-9c-E1-56 -60-CB} |
| PASTA de \_ UserProgramFilesCommon | {bcbd3057-ca5c-4622-B4-2D-BC-56-DB-0A-E5-16} |
| Vídeos de FOLDERid \_                 | {18989B1D-99B5-455B-84-1C-AB-7C-74-E4-DD-FC} |
| FOLDERid \_ VideosLibrary {        | 491e922f-5643-4af4-a7-EB-4e-7a-13-8D-81-74}  |
| FOLDERid \_ Windows {              | F38BF404-1D43-42F2-93-05 -67-DE-0B-28-FC-23}  |



 

## <a name="examples"></a>Exemplos


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```




```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)
</dt> </dl>

 

 
