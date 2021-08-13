---
description: O objeto Product representa uma instância exclusiva de um produto anunciado, instalado ou desconhecido. O objeto pode ser instariado com a propriedade Product como &\# 0034; WindowsInstaller.Installer.Product(ProductCode, UserSid, Context)&\# 0034;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Objeto product
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ff05a2f89244da09caa6cd3b26fc4b5d9cdbec95c0fcc3098fddf0c39dc68519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627669"
---
# <a name="product-object"></a>Objeto product

O **objeto** Product representa uma instância exclusiva de um produto anunciado, instalado ou desconhecido.

O objeto pode ser instalá-lo com a propriedade Product como "WindowsInstaller.Installer.Product(*ProductCode,*  *UserSid*, *Context*)". *UserSid* deve ser NULL para o contexto por computador. *UserSid* pode ser nulo para o usuário atual especificado, quando o contexto não é por computador. *Os parâmetros ProductCode* e *Context* são necessários.

## <a name="members"></a>Membros

O **objeto** Product tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto** Product tem esses métodos.



| Método                                                                 | Descrição                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)       | Adicione um disco ao conjunto de discos registrados.<br/>                                                              |
| [**SourceListAddSource**](product-sourcelistaddsource.md)             | Adicione uma fonte de rede ou URL à lista de origem.<br/>                                                         |
| [**SourceListClearAll**](product-sourcelistclearall.md)               | Limpa a lista de origem completa do tipo de fontes especificado.<br/>                                       |
| [**SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)   | Remova um disco do conjunto de discos registrados da lista de origem.<br/>                                    |
| [**SourceListClearSource**](product-sourcelistclearsource.md)         | Remova uma fonte de rede ou URL da lista de origem.<br/>                                                    |
| [**SourceListForceResolution**](product-sourcelistforceresolution.md) | Limpa a última fonte usada. Isso força uma resolução de lista de origem na próxima vez que a origem for necessária.<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto Product** tem essas propriedades.



| Propriedade                                                      | Descrição                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**ComponentState**](product-componentstate.md)<br/>   | O estado de um componente especificado para esta instância do produto. <br/>                   |
| [**Contexto**](product-context.md)<br/>                 | Contexto dessa instância do produto como um valor MSIINSTALLCONTEXT. <br/>                 |
| [**FeatureState**](product-featurestate.md)<br/>       | O estado de um recurso especificado para esta instância do produto. <br/>                     |
| [**InstallProperty**](product-installproperty.md)<br/> | O valor de uma propriedade especificada. <br/>                                              |
| [**MediaDisks**](product-mediadisks.md)<br/>           | Enumera todos os discos de mídia para esta instância do produto.<br/>                        |
| [**ProductCode**](product-productcode.md)<br/>         | Retorna o código do produto. <br/>                                                       |
| [**SourceListInfo**](product-sourcelistinfo.md)<br/>   | Obter e definir as propriedades de informações de origem. Essa é uma propriedade de leitura ou gravação.<br/> |
| [**Fontes**](product-sources.md)<br/>                 | Enumera todas as fontes para esta instância do produto.<br/>                            |
| [**Estado**](product-state.md)<br/>                     | Estado de instalação do produto.<br/>                                               |
| [**UserSid**](product-usersid.md)<br/>                 | Retorna o SID do usuário, sob qual conta esta instância do produto está disponível.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador 3.0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct é definido como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




