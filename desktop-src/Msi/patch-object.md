---
description: O objeto patch representa uma instância exclusiva de um patch que foi registrado ou aplicado. O objeto pode ser instanciado com a propriedade patch como &\# 0034; WindowsInstaller. Installer. patch (PatchCode, ProductCode, userid, contexto) &\# 0034;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Objeto patch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6fa55d6ced2afdc53ef8050732f5dee5d6c1f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751641"
---
# <a name="patch-object"></a>Objeto patch

O objeto **patch** representa uma instância exclusiva de um patch que foi registrado ou aplicado.

O objeto pode ser instanciado com a propriedade **patch** como "WindowsInstaller. Installer. patch (*PatchCode*, *ProductCode*, *userid*, *Context*)". Para um contexto de computador, o parâmetro *userid* deve ser uma cadeia de caracteres vazia. O *ProductCode* pode ser definido como uma cadeia de caracteres vazia para patches que são registrados apenas e que ainda não foram aplicados a nenhum produto. O *ProductCode* pode ser definido como uma cadeia de caracteres vazia ao ler ou atualizar informações da lista de origem de um patch.

## <a name="members"></a>Membros

O objeto **patch** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **patch** tem esses métodos.



| Método                                                               | Descrição                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)       | Adicione um disco ao conjunto de discos registrados.<br/>                                                                                   |
| [**SourceListAddSource**](patch-sourcelistaddsource.md)             | Adicione uma fonte de rede ou URL à lista de origem. <br/>                                                                             |
| [**SourceListClearAll**](patch-sourcelistclearall.md)               | Limpa a lista de origem completa do tipo de fontes especificado.<br/>                                                            |
| [**SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)   | Remova um disco do conjunto de discos registrados da lista de origem. <br/>                                                        |
| [**SourceListClearSource**](patch-sourcelistclearsource.md)         | Remova uma rede ou origem da URL da lista de origem.<br/>                                                                         |
| [**SourceListForceResolution**](patch-sourcelistforceresolution.md) | Limpa a última fonte usada da lista de origem. Isso forçará uma resolução da lista de origem na próxima vez em que a origem for necessária.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **patch** tem essas propriedades.



| Propriedade                                                  | Descrição                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Contexto**](patch-context.md)<br/>               | O contexto dessa instância de patch é um valor de MSIINSTALLCONTEXT.<br/>                                   |
| [**MediaDisks**](patch-mediadisks.md)<br/>         | Enumera todos os discos de mídia para esta instância de patch.<br/>                                         |
| [**PatchCode**](patch-patchcode.md)<br/>           | Retorna o código do patch.<br/>                                                                         |
| [**Patchproperty**](patch-patchproperty.md)<br/>   | Obtém informações de propriedade sobre um patch específico aplicado a uma instância específica do produto.<br/> |
| [**ProductCode**](patch-productcode.md)<br/>       | Retorna o código do produto.<br/>                                                                       |
| [**SourceListInfo**](patch-sourcelistinfo.md)<br/> | Obtém e define as propriedades de informações de origem. Esta é uma propriedade de leitura ou gravação.<br/>              |
| [**Fontes**](patch-sources.md)<br/>               | Enumera todas as fontes para esta instância de patch.<br/>                                             |
| [**Status**](patch-state.md)<br/>                   | Estado da instalação do patch.<br/>                                                                |
| [**UserSid**](patch-usersid.md)<br/>               | Retorna o SID do usuário, na conta em que esta instância de patch está disponível.<br/>                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




