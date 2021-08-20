---
title: Método ImportLicenseKeyPackOffline da classe Win32_TSLicenseKeyPack
description: Importa, de outro servidor de Área de Trabalho Remota licença, um Serviços de Área de Trabalho Remota de chaves de licença que usa um identificador de licença que foi recebido pela Internet ou pelo telefone.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- Método ImportLicenseKeyPackOffline Serviços de Área de Trabalho Remota
- Método ImportLicenseKeyPackOffline Serviços de Área de Trabalho Remota , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Serviços de Área de Trabalho Remota , método ImportLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7d5be5dc8cfd9f654c09d989149a423351689f420a52ca1756fb197260e800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348627"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Método ImportLicenseKeyPackOffline da classe \_ TSLicenseKeyPack do Win32

Importa, de outro servidor de Área de Trabalho Remota licença, um Serviços de Área de Trabalho Remota de chaves de licença que usa um identificador de licença que foi recebido pela Internet ou pelo telefone.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sLicenseKeyPackId* \[ Em\]
</dt> <dd>

Contém o código de licença de 35 caracteres. Somente a cadeia de caracteres alfanuméricos de 35 caracteres deve ser dada como entrada. Nenhum hífen deve ser adicionado.

</dd> <dt>

*sSourceLSName* \[ Em\]
</dt> <dd>

O nome do servidor de Área de Trabalho Remota de origem. Esse é o nome diferenciado totalmente qualificado ou o endereço IP do servidor.

</dd> <dt>

*sSourceLSProductId* \[ Em\]
</dt> <dd>

O Área de Trabalho Remota do servidor de licença. O é uma cadeia de caracteres alfanumérico de 35 caracteres que não pode incluir hifens.

</dd> <dt>

*KeyPackId* \[ out\]
</dt> <dd>

Recebe o identificador do pacote de chaves.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





