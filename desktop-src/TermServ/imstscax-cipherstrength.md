---
title: Propriedade IMsTscAx CipherStrength
description: Recupera a intensidade máxima de criptografia do controle atual.
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, propriedade CipherStrength
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
ms.openlocfilehash: 401cf3796d349aaa6764eae46a371a9d485f763c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369303"
---
# <a name="imstscaxcipherstrength-property"></a>Propriedade IMsTscAx:: CipherStrength

Recupera a intensidade máxima de criptografia do controle atual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a>Valor da propriedade

O nível de criptografia.

## <a name="error-codes"></a>Códigos do Erro

Retornar **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

Por Conexão Web de Área de Trabalho Remota, a intensidade de codificação é sempre 128 porque o controle ActiveX Área de Trabalho Remota dá suporte à criptografia até e incluindo 128 bits. O controle de 128 bits ainda pode se conectar a servidores de Host da Sessão da Área de Trabalho Remota de criptografia de 56 bits (Host da Sessão RD).

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





