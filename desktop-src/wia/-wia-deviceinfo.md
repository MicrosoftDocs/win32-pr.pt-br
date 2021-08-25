---
description: O objeto DeviceInfo fornece acesso às propriedades de um dispositivo de hardware WIA (Aquisição de Imagem Windows Imagem).
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
ms.openlocfilehash: 69b34a97483a8a6ce231890454148c7948f63e4e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467173"
---
# <a name="deviceinfo-object"></a>Objeto DeviceInfo

O **objeto DeviceInfo** fornece acesso às propriedades de um dispositivo de hardware WIA (Aquisição de Imagem Windows). Ele também, por meio de [**seu método Create,**](-wia-iwiadeviceinfo-create.md) fornece uma maneira para o aplicativo ou script se conectar ao dispositivo e obter um [**objeto Item**](-wia-item.md) que representa o dispositivo. Use o [**método Devices**](-wia-iwia-devices.md) para obter uma coleção de **objetos DeviceInfo.**

## <a name="members"></a>Membros

O **objeto DeviceInfo** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto DeviceInfo** tem esses métodos.



| Método                                                 | Descrição                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Criar**](-wia-iwiadeviceinfo-create.md)           | O [**método**](-wia-iwiadeviceinfo-create.md) Create do **objeto DeviceInfo** faz uma conexão com o dispositivo WIA especificado pelo **objeto DeviceInfo** e retorna um [**objeto Item**](-wia-item.md) que representa o dispositivo.<br/> |
| [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) | O [**método GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) do **objeto DeviceInfo** usa a ID de uma propriedade de dispositivo para retornar seu valor.<br/>                                                                                               |



 

### <a name="properties"></a>Propriedades

O **objeto DeviceInfo** tem essas propriedades.




| Propriedade | Tipo de acesso | Descrição | 
|----------|-------------|-------------|
| <a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a><br /> | Somente leitura<br /> | Recupera a ID do dispositivo de hardware WIA. <br /> | 
| <a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Fabricante</strong></a><br /> | Somente leitura<br /> | Recupera o nome do fabricante deste dispositivo de hardware.<br /> | 
| <a href="-wia-iwiadeviceinfo-name.md"><strong>Nome</strong></a><br /> | Somente leitura<br /> | O nome do dispositivo de hardware WIA como ele aparece na interface do usuário.<br /> | 
| <a href="-wia-iwiadeviceinfo-port.md"><strong>Porta</strong></a><br /> | Somente leitura<br /> | Recupera a porta à qual o dispositivo de hardware WIA está conectado.<br /> | 
| <a href="-wia-iwiadeviceinfo-type.md"><strong>Type</strong></a><br /> | Somente leitura<br /> | Recupera o tipo de dispositivo de hardware WIA. Os valores possíveis são: <br /><ul><li>DigitalCamera</li><li>Scanner</li><li>StreamingVideo</li><li>Padrão</li></ul> | 
| <a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a><br /> | Somente leitura<br /> | Recupera a ID de classe da interface do usuário fornecida pelo fabricante para este dispositivo de hardware WIA. O valor é uma representação de cadeia de caracteres de um GUID. <br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4.90 ou posterior)</dt> </dl> |



 

 




