---
description: Windows Os dispositivos portáteis oferecem suporte às seguintes propriedades de extensão de classe.
ms.assetid: 9b8983ba-5824-495d-868f-fd22b98e1954
title: Propriedades de extensão de classe (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Class
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c7215a383aec582f576cb64a6781068034bb7fa8df03b5a404368482f1c1619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843400"
---
# <a name="class-extension-properties"></a>Propriedades de extensão de classe

Windows Os dispositivos portáteis oferecem suporte às seguintes propriedades de extensão de classe.



| Propriedade                                                                      | VarType         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_Opções de extensão de classe WPD \_ \_ \_ com suporte \_ tipos de conteúdo \_**                 | **VT \_ desconhecido** | Um valor que especifica a lista (superconjunto) de tipos de conteúdo com suporte pelo driver (semelhante à chamada de \_ recursos de comando WPD \_ \_ obter tipos de \_ conteúdo com suporte \_ \_ na **\_ categoria funcional de WPD \_ \_ todos**).                                                                                                                                                                                                                                                                                                                                             |
| **\_as opções de extensão de classe WPD não \_ \_ \_ \_ registram a \_ interface de \_ dispositivo WPD \_**    | **BOOL do VT \_**    | Um valor que especifica se o chamador deseja que a biblioteca de extensão de classe WPD Registre a interface de classe de dispositivo WPD. Se esse valor for true, o chamador será responsável pelo registro.<br/> Se esse valor for false, ele indicará que o chamador espera que a biblioteca de extensão de classe execute o registro.<br/>A maioria dos drivers deve permitir que a biblioteca de extensão de classe execute o registro, exceto onde registrar a interface de classe de dispositivo WPD pela biblioteca de extensão de classe pode causar efeitos adversos. |
| **\_Opções de extensão de classe WPD registrar a \_ \_ \_ \_ \_ interface de dispositivo particular WPD \_ \_** | **BOOL do VT \_**    | Indica que o chamador deseja que a biblioteca de extensão de classe WPD Registre a interface de classe de dispositivo de WPD particular. Isso não é recomendado para a maioria dos drivers. Ele só deve ser usado em casos em que o registro da interface de classe do dispositivo WPD pela biblioteca de extensão de classe causará efeitos adversos. Essa opção é normalmente usada em conjunto com **\_ as opções de extensão de classe WPD não \_ registrar a \_ \_ \_ \_ \_ \_ interface de dispositivo WPD** definida como **true**                                                                                          |
| **\_extensão de classe WPD \_ \_ Opções valores de \_ identificação de dispositivo \_ \_**            | **VT \_ desconhecido** | Este é um [IPortableDeviceValues](iportabledevicevalues.md) que contém os valores de identificação do dispositivo (**\_ \_ fabricante do dispositivo WPD**, **\_ \_ modelo de dispositivo WPD**, **versão do \_ firmware do dispositivo \_ \_ WPD** e **\_ \_ \_ \_ ID exclusiva funcional do dispositivo WPD**). Incluir isso com outras opções de extensão de classe ao inicializar                                                                                                                                                                                                                               |
| **\_Opções de extensão de classe WPD largura de \_ \_ \_ banda de transporte \_**                      | **\_UI4 VT**     | Indica a largura de banda teórica máxima do transporte em quilobits por segundo                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **\_extensão de classe WPD \_ \_ Opções valores de \_ identificação de dispositivo \_ \_**            | **VT \_ desconhecido** | Este é um [IPortableDeviceValues](iportabledevicevalues.md) que contém os valores de identificação do dispositivo (**\_ \_ fabricante do dispositivo WPD**, **\_ \_ modelo de dispositivo WPD**, **versão do \_ firmware do dispositivo \_ \_ WPD** e **\_ \_ \_ \_ ID exclusiva funcional do dispositivo WPD**). Inclua isso com outras opções de extensão de classe ao inicializar.                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




