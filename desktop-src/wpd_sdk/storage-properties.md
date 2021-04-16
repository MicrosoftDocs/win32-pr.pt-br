---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de armazenamento.
ms.assetid: 234078c3-e703-41f3-9b18-ae61d8a36784
title: Propriedades de armazenamento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Storage
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 404b45a6fe5193a0550b3ecc11feeae264125110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773010"
---
# <a name="storage-properties"></a>Propriedades de armazenamento

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de armazenamento.



| Propriedade                                   | VarType        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_capacidade de armazenamento WPD \_**                 | **\_UI8 VT**    | A capacidade de armazenamento total, em bytes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **\_ \_ capacidade de armazenamento WPD \_ em \_ objetos**    | **\_UI8 VT**    | Indica a capacidade de armazenamento total em objetos; por exemplo, os slots disponíveis em um cartão SIM.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **\_Descrição do armazenamento WPD \_**              | **LPWStr do VT \_** | Uma descrição legível do armazenamento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_tipo de \_ sistema de arquivos de armazenamento WPD \_ \_**       | **LPWStr do VT \_** | Uma descrição da cadeia de caracteres do sistema de arquivos usado pelo armazenamento, por exemplo, "FAT32", "NTFS", "sistema de arquivos contoso" e assim por diante.                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_ \_ espaço livre de armazenamento WPD \_ \_ em \_ bytes**   | **\_UI8 VT**    | O espaço de armazenamento disponível, em bytes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **\_ \_ espaço livre de armazenamento WPD \_ \_ em \_ objetos** | **\_UI8 VT**    | O número de objetos adicionais que podem ser gravados no dispositivo. Por exemplo, se um dispositivo permitir apenas um único objeto, isso seria zero se o objeto já existisse.                                                                                                                                                                                                                                                                                                                                                          |
| **\_número de \_ série de armazenamento WPD \_**           | **LPWStr do VT \_** | Um número de série específico do fornecedor para o armazenamento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **\_ \_ tamanho máximo de \_ objeto de armazenamento WPD \_**        | **\_UI8 VT**    | Especifica o tamanho máximo de um único objeto, em bytes, que pode ser colocado nesse armazenamento.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_tipo de armazenamento WPD \_**                     | **\_UI4 VT**    | Descreve o tipo físico de um meio de armazenamento de memória.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_recurso de \_ acesso de armazenamento WPD \_**       | **\_UI4 VT**    | Identifica qualquer proteção contra gravação que afete globalmente esse armazenamento. Isso tem precedência sobre o acesso especificado em objetos individuais. Os valores possíveis são da enumeração de **valores de capacidade de \_ acesso de armazenamento \_ \_ \_ WPD** definida em PortableDevice. h. Por exemplo, se **o \_ \_ tipo de armazenamento WPD** for ROM (que é um **tipo de armazenamento WPD de ROM \_ \_ \_ fixa \_** ou de **\_ tipo de armazenamento \_ \_ \_** wpd), o valor da **funcionalidade de \_ \_ acesso \_ de armazenamento** WPD deve ser um **recurso de acesso de \_ armazenamento WPD \_ \_ \_ \_ somente leitura \_ sem \_ \_ exclusão de objeto**. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




