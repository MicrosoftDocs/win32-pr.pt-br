---
title: Propriedade IMsRdpClientNonScriptable4 PublisherCertificateChain
description: Controla a cadeia de certificados do Publicador. A cadeia é armazenada em uma variante do tipo VT \_ ByRef que contém um ponteiro para uma \_ estrutura de contexto de cadeia de certificados \_ . Para obter informações sobre as \_ estruturas ByRef do VT, consulte VARIANT e VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade PublisherCertificateChain
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824548"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a>IMsRdpClientNonScriptable4: Propriedade ublisherCertificateChain de:P

Controla a cadeia de certificados do Publicador. A cadeia é armazenada em uma variante do tipo **VT \_ ByRef** que contém um ponteiro para uma estrutura de [**\_ \_ contexto de cadeia de certificados**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) . Para obter informações sobre as estruturas **\_ ByRef do VT** , consulte [Variant e VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a>Valor da propriedade

Define a cadeia de certificados do Publicador. A cadeia é armazenada em uma variante do tipo **VT \_ ByRef** que contém um ponteiro para uma estrutura de [**\_ \_ contexto de cadeia de certificados**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 é definido como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

