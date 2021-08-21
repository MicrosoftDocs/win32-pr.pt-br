---
title: Propriedade IMsTscAx DesktopWidth
description: Especifica a largura do controle atual, em pixels, na área de trabalho remota inicial.
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade DesktopWidth
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca982303208bb2badecf210c9590f627a7b3b57c5acd9ecd7f8fee0bbb70ec93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058834"
---
# <a name="imstscaxdesktopwidth-property"></a>IMsTscAx: Propriedade esktopWidth de:D

Especifica a largura do controle atual, em pixels, na área de trabalho remota inicial.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

A nova largura, em pixels.

## <a name="error-codes"></a>Códigos do Erro

Retornar **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

a definição da propriedade **DesktopWidth** é opcional, mas deve ser definida antes de chamar o método [**Conexão**](imstscax-connect.md) . Se uma largura de área de trabalho não for especificada ou for definida como zero, a largura da área de trabalho será definida com a largura do controle. Os valores mínimo e máximo dependem da versão do sistema operacional do cliente de Área de Trabalho Remota.

<dl> <dt>

<span id="_"></span>Windows 8/Windows Server 2012
</dt> <dd>

mínimo de 200, 8192 máximo

</dd> <dt>

<span id="_"></span>Windows 7/Windows Server 2008
</dt> <dd>

mínimo de 200, 2048 máximo

</dd> <dt>

Windows Vista
</dt> <dd>

mínimo de 200, 1200 máximo

</dd> </dl>

Depois que uma conexão é estabelecida, as alterações na largura do controle não alteram a largura da área de trabalho remota. Em vez disso, o controle abre as barras de rolagem ou centraliza a área de trabalho remota, conforme apropriado. Para alterar o tamanho da área de trabalho de uma conexão ativa, use o método [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .

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

 

 





