---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de associação de rede.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Propriedades de associação de rede (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810831"
---
# <a name="network-association-properties"></a>Propriedades de associação de rede

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de associação de rede.



| Propriedade                                                  | VarType                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ \_ identificadores de rede do host de associação de rede WPD \_** | **\_UI1 de vetor \| VT \_ VT** | A lista de identificadores de host EUI-64 válidos para esta associação. Esta é uma matriz de bytes que contém um número integral de endereços de rede física EUI-64. Esses valores EUI-64 são os endereços de rede física disponíveis no host no momento da Associação de rede. Se o host tiver endereços de rede física MAC-48 (típicos de redes IPv4), cada endereço MAC-48 será codificado no endereço EUI-64 como as duas metades do endereço MAC-48 separados por FF-FF.<br/> |
| **\_X509V3SEQUENCE de \_ Associação de rede WPD \_**             | **\_UI1 de vetor \| VT \_ VT** | A sequência de certificados X. 509 v3 a serem fornecidos para a autenticação do servidor TLS.                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




