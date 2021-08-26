---
title: Propriedade CipherStrength IMsTscAx
description: Recupera a intensidade máxima de criptografia do controle atual.
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- Propriedade CipherStrength Serviços de Área de Trabalho Remota
- Propriedade CipherStrength Serviços de Área de Trabalho Remota , interface IMsTscAx
- Interface IMsTscAx Serviços de Área de Trabalho Remota , propriedade CipherStrength
- A propriedade CipherStrength Serviços de Área de Trabalho Remota , interface IMsRdpClient
- Interface IMsRdpClient Serviços de Área de Trabalho Remota , propriedade CipherStrength
- A propriedade CipherStrength Serviços de Área de Trabalho Remota , interface IMsRdpClient2
- Interface IMsRdpClient2 Serviços de Área de Trabalho Remota , propriedade CipherStrength
- A propriedade CipherStrength Serviços de Área de Trabalho Remota , interface IMsRdpClient3
- Interface IMsRdpClient3 Serviços de Área de Trabalho Remota , propriedade CipherStrength
- A propriedade CipherStrength Serviços de Área de Trabalho Remota , interface IMsRdpClient4
- Interface IMsRdpClient4 Serviços de Área de Trabalho Remota propriedade , CipherStrength
- A propriedade CipherStrength Serviços de Área de Trabalho Remota , interface IMsRdpClient5
- Interface IMsRdpClient5 Serviços de Área de Trabalho Remota propriedade , CipherStrength
- A propriedade CipherStrength Serviços de Área de Trabalho Remota , interface IMsRdpClient6
- Interface IMsRdpClient6 Serviços de Área de Trabalho Remota , propriedade CipherStrength
- A propriedade CipherStrength Serviços de Área de Trabalho Remota , interface IMsRdpClient7
- Interface IMsRdpClient7 Serviços de Área de Trabalho Remota , propriedade CipherStrength
- A propriedade CipherStrength Serviços de Área de Trabalho Remota , interface IMsRdpClient8
- Interface IMsRdpClient8 Serviços de Área de Trabalho Remota , propriedade CipherStrength
- A propriedade CipherStrength Serviços de Área de Trabalho Remota , interface IMsRdpClient9
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota propriedade , CipherStrength
topic_type:
- apiref
api_name:
- IMsTscAx.CipherStrength
- IMsTscAx.get_CipherStrength
- IMsRdpClient.CipherStrength
- IMsRdpClient.get_CipherStrength
- IMsRdpClient2.CipherStrength
- IMsRdpClient2.get_CipherStrength
- IMsRdpClient3.CipherStrength
- IMsRdpClient3.get_CipherStrength
- IMsRdpClient4.CipherStrength
- IMsRdpClient4.get_CipherStrength
- IMsRdpClient5.CipherStrength
- IMsRdpClient5.get_CipherStrength
- IMsRdpClient6.CipherStrength
- IMsRdpClient6.get_CipherStrength
- IMsRdpClient7.CipherStrength
- IMsRdpClient7.get_CipherStrength
- IMsRdpClient8.CipherStrength
- IMsRdpClient8.get_CipherStrength
- IMsRdpClient9.CipherStrength
- IMsRdpClient9.get_CipherStrength
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b66418f2e956afcf6c5b9f1f9a0d5971119e7fddae1c1d46d115f4bbe0e6391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125436"
---
# <a name="imstscaxcipherstrength-property"></a>Propriedade IMsTscAx::CipherStrength

Recupera a intensidade máxima de criptografia do controle atual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a>Valor da propriedade

A intensidade de criptografia.

## <a name="error-codes"></a>Códigos do Erro

Retornar **S \_ OK se** for bem-sucedido.

## <a name="remarks"></a>Comentários

Por Conexão Web de Área de Trabalho Remota, a força da codificação é sempre 128 porque o controle Área de Trabalho Remota ActiveX dá suporte à criptografia de até 128 bits e incluindo 128 bits. O controle de 128 bits ainda pode se conectar a servidores de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) de criptografia de 56 bits.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsTscAx é definido como \_ 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Imsrdpclient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> </dl>

 

 





