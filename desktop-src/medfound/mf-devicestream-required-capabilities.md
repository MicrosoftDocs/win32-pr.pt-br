---
description: Especifica uma lista de cadeias de caracteres Unicode que representam os recursos do dispositivo exigidos pela transformação do sensor.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: Atributo MF_DEVICESTREAM_REQUIRED_CAPABILITIES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090691"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a>\_Atributo de \_ \_ funcionalidades necessárias do MF DEVICESTREAM

Especifica uma lista de cadeias de caracteres Unicode que representam os recursos do dispositivo exigidos pela transformação do sensor.

## <a name="data-type"></a>Tipo de dados

**WCHAR \** _

## <a name="remarks"></a>Comentários

Esse atributo é opcional e só será necessário se a transformação do sensor acessar um recurso protegido. O valor deve ser uma lista delimitada por ponto e vírgula de tokens de cadeia de caracteres definidos em [_ *DeviceCapability* *](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
