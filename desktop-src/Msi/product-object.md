---
description: O objeto Product representa uma instância exclusiva de um produto que é anunciado, instalado ou desconhecido. O objeto pode ser instanciado com a Propriedade Product como &\# 0034; WindowsInstaller. Installer. Product (ProductCode, userid, contexto) &\# 0034;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Objeto Product
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
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747953"
---
# <a name="product-object"></a>Objeto Product

O objeto **Product** representa uma instância exclusiva de um produto que é anunciado, instalado ou desconhecido.

O objeto pode ser instanciado com a propriedade **Product** como "WindowsInstaller. Installer. Product (*ProductCode*, *userid*, *Context*)". *Userid* deve ser nulo para o contexto por máquina. O *userid* pode ser nulo para o usuário atual especificado, quando o contexto não for por computador. Os parâmetros de *ProductCode* e de *contexto* são obrigatórios.

## <a name="members"></a>Membros

O objeto **Product** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Product** tem esses métodos.



| Método                                                                 | Descrição                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)       | Adicione um disco ao conjunto de discos registrados.<br/>                                                              |
| [**SourceListAddSource**](product-sourcelistaddsource.md)             | Adicione uma fonte de rede ou URL à lista de origem.<br/>                                                         |
| [**SourceListClearAll**](product-sourcelistclearall.md)               | Limpa a lista de origem completa do tipo de fontes especificado.<br/>                                       |
| [**SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)   | Remova um disco do conjunto de discos registrados da lista de origem.<br/>                                    |
| [**SourceListClearSource**](product-sourcelistclearsource.md)         | Remova uma rede ou origem da URL da lista de origem.<br/>                                                    |
| [**SourceListForceResolution**](product-sourcelistforceresolution.md) | Limpa a última fonte usada. Isso forçará uma resolução da lista de origem na próxima vez em que a origem for necessária.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **Product** tem essas propriedades.



| Propriedade                                                      | Descrição                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Componentestate**](product-componentstate.md)<br/>   | O estado de um componente especificado para esta instância de produto. <br/>                   |
| [**Contexto**](product-context.md)<br/>                 | Contexto desta instância de produto como um valor de MSIINSTALLCONTEXT. <br/>                 |
| [**Recurso**](product-featurestate.md)<br/>       | O estado de um recurso especificado para esta instância do produto. <br/>                     |
| [**Instalar a**](product-installproperty.md)<br/> | O valor de uma propriedade especificada. <br/>                                              |
| [**MediaDisks**](product-mediadisks.md)<br/>           | Enumera todos os discos de mídia para esta instância de produto.<br/>                        |
| [**ProductCode**](product-productcode.md)<br/>         | Retorna o código do produto. <br/>                                                       |
| [**SourceListInfo**](product-sourcelistinfo.md)<br/>   | Obter e definir as propriedades de informações de origem. Esta é uma propriedade de leitura ou gravação.<br/> |
| [**Fontes**](product-sources.md)<br/>                 | Enumera todas as fontes para esta instância do produto.<br/>                            |
| [**Status**](product-state.md)<br/>                     | Estado de instalação do produto.<br/>                                               |
| [**UserSid**](product-usersid.md)<br/>                 | Retorna o SID de usuário, sob a qual conta esta instância de produto está disponível.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




