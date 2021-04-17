---
description: O objeto DeviceInfo fornece acesso às propriedades de um dispositivo de hardware de aquisição de imagem do Windows (WIA).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Objeto DeviceInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748303"
---
# <a name="deviceinfo-object"></a>Objeto DeviceInfo

O objeto **DeviceInfo** fornece acesso às propriedades de um dispositivo de hardware de aquisição de imagem do Windows (WIA). Ele também, por meio de seu método [**Create**](-wia-iwiadeviceinfo-create.md) , fornece uma maneira para o aplicativo ou script se conectar ao dispositivo e obter um objeto [**Item**](-wia-item.md) que representa o dispositivo. Use o método [**Devices**](-wia-iwia-devices.md) para obter uma coleção de objetos **DeviceInfo** .

## <a name="members"></a>Membros

O objeto **DeviceInfo** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **DeviceInfo** tem esses métodos.



| Método                                                 | Descrição                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Criada**](-wia-iwiadeviceinfo-create.md)           | O método [**Create**](-wia-iwiadeviceinfo-create.md) do objeto **DeviceInfo** faz uma conexão com o dispositivo WIA especificado pelo objeto **DeviceInfo** e retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo.<br/> |
| [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) | O método [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) do objeto **DEVICEINFO** usa a ID de uma propriedade de dispositivo para retornar seu valor.<br/>                                                                                               |



 

### <a name="properties"></a>Propriedades

O objeto **DeviceInfo** tem essas propriedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriedade</th>
<th style="text-align: left;">Tipo de acesso</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-id.md"><strong>Sessão</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Recupera a ID do dispositivo de hardware WIA. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Manufacturer</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Recupera o nome do fabricante deste dispositivo de hardware.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-name.md"><strong>Nome</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">O nome do dispositivo de hardware WIA como ele aparece na interface do usuário.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-port.md"><strong>Porta</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Recupera a porta à qual o dispositivo de hardware WIA está conectado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-type.md"><strong>Tipo</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Recupera o tipo de dispositivo de hardware WIA. Os valores possíveis são: <br/>
<ul>
<li>DigitalCamera</li>
<li>Scanner</li>
<li>StreamingVideo</li>
<li>Padrão</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Recupera a ID de classe da interface do usuário fornecida pelo fabricante para este dispositivo de hardware WIA. O valor é uma representação de cadeia de caracteres de um GUID. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




