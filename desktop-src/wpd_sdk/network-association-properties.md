---
description: Windows Os Dispositivos Portáteis são compatíveis com as seguintes propriedades de associação de rede.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Propriedades de associação de rede (PortableDevice.h)
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
ms.openlocfilehash: ebad4534976d14e6b620a8e42b70e8ece68022201cec5235295d199e453ef818
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963525"
---
# <a name="network-association-properties"></a>Propriedades de associação de rede

Windows Os Dispositivos Portáteis são compatíveis com as seguintes propriedades de associação de rede.



| Propriedade                                                  | VarType                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IDENTIFICADORES DE REDE DE HOST DE ASSOCIAÇÃO \_ \_ \_ \_ \_ DE REDE WPD** | **VT \_ VECTOR \| VT \_ UI1** | A lista de identificadores de host EUI-64 válidos para essa associação. Essa é uma matriz de bytes que contém um número integral de endereços de rede física EUI-64. Esses valores EUI-64 são os endereços de rede física disponíveis no host no momento da Associação de Rede. Se o host tiver endereços de rede física MAC-48 (típicos de redes IPv4), cada endereço MAC-48 será codificado no endereço EUI-64 como as duas metades do endereço MAC-48 separados por FF-FF.<br/> |
| **WPD \_ NETWORK \_ ASSOCIATION \_ X509V3SEQUENCE**             | **VT \_ VECTOR \| VT \_ UI1** | A sequência de certificados X.509 v3 a serem fornecidos para autenticação de servidor TLS.                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




