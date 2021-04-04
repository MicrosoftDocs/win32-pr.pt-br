---
title: Método ReinstallLicenseKeyPackOffline da classe Win32_TSLicenseKeyPack
description: Reinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa o identificador de licença que foi recebido pela Internet ou pelo telefone.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ReinstallLicenseKeyPackOffline
- Método ReinstallLicenseKeyPackOffline Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ReinstallLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e805521ea750c018ab2e7965e7fbfba05a92d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824212"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Método ReinstallLicenseKeyPackOffline da classe Win32 \_ TSLicenseKeyPack

Reinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa o identificador de licença que foi recebido pela Internet ou pelo telefone.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sLicenseKeyPackId* \[ no\]
</dt> <dd>

Contém o código de licença de 35 caracteres. Somente a cadeia de caracteres alfanumérica de 35 caracteres deve ser fornecida como entrada. Nenhum hífen deve ser adicionado.

</dd> <dt>

*Pacote de chaves* \[ fora\]
</dt> <dd>

Recebe o identificador do pacote de chaves.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





