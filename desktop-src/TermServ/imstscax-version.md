---
title: Propriedade de versão IMsTscAx
description: Especifica o número de versão do controle atual.
ms.assetid: 91ddeb4c-9d61-41e7-af96-95b0c4884682
ms.tgt_platform: multiple
keywords:
- Propriedade version Serviços de Área de Trabalho Remota
- Propriedade version Serviços de Área de Trabalho Remota , interface IMsTscAx
- Interface IMsTscAx Serviços de Área de Trabalho Remota , propriedade Version
- A propriedade version Serviços de Área de Trabalho Remota , interface IMsRdpClient
- Interface IMsRdpClient Serviços de Área de Trabalho Remota propriedade , Versão
- A propriedade version Serviços de Área de Trabalho Remota interface , IMsRdpClient2
- Interface IMsRdpClient2 Serviços de Área de Trabalho Remota propriedade , Versão
- A propriedade version Serviços de Área de Trabalho Remota , interface IMsRdpClient3
- Interface IMsRdpClient3 Serviços de Área de Trabalho Remota propriedade , Versão
- A propriedade version Serviços de Área de Trabalho Remota interface , IMsRdpClient4
- Interface IMsRdpClient4 Serviços de Área de Trabalho Remota , propriedade Version
- A propriedade version Serviços de Área de Trabalho Remota , interface IMsRdpClient5
- Interface IMsRdpClient5 Serviços de Área de Trabalho Remota propriedade , Versão
- A propriedade version Serviços de Área de Trabalho Remota interface , IMsRdpClient6
- Interface IMsRdpClient6 Serviços de Área de Trabalho Remota , propriedade Version
- A propriedade version Serviços de Área de Trabalho Remota , interface IMsRdpClient7
- Interface IMsRdpClient7 Serviços de Área de Trabalho Remota , propriedade Version
- A propriedade version Serviços de Área de Trabalho Remota , interface IMsRdpClient8
- Interface IMsRdpClient8 Serviços de Área de Trabalho Remota , propriedade Version
- A propriedade version Serviços de Área de Trabalho Remota , interface IMsRdpClient9
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota , propriedade Version
topic_type:
- apiref
api_name:
- IMsTscAx.Version
- IMsTscAx.get_Version
- IMsRdpClient.Version
- IMsRdpClient.get_Version
- IMsRdpClient2.Version
- IMsRdpClient2.get_Version
- IMsRdpClient3.Version
- IMsRdpClient3.get_Version
- IMsRdpClient4.Version
- IMsRdpClient4.get_Version
- IMsRdpClient5.Version
- IMsRdpClient5.get_Version
- IMsRdpClient6.Version
- IMsRdpClient6.get_Version
- IMsRdpClient7.Version
- IMsRdpClient7.get_Version
- IMsRdpClient8.Version
- IMsRdpClient8.get_Version
- IMsRdpClient9.Version
- IMsRdpClient9.get_Version
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8911eaaf8af95e0f3ca1fde254250bcc781e71450b7d96ce8dc342b36298d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770846"
---
# <a name="imstscaxversion-property"></a>Propriedade IMsTscAx::Version

Especifica o número de versão do controle atual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Version(
  [out] BSTR *pVersion
);
```



## <a name="property-value"></a>Valor da propriedade

O número de versão.

## <a name="error-codes"></a>Códigos do Erro

Retornar **S \_ OK se** for bem-sucedido.

## <a name="remarks"></a>Comentários

Esse método aloca a memória necessária para o buffer apontado pelo *parâmetro pVersion.* Chamar aplicativos C/C++ deve liberar a memória com uma chamada para a [**função SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) Isso não é necessário para clientes Visual Basic e scripts.

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

 

