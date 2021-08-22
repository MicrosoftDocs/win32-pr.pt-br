---
title: Método FetchReportPerDeviceEntries da classe Win32_TSLicenseReport dados
description: Recupera informações de licenças de acesso do cliente Serviços de Área de Trabalho Remota por dispositivo (RDS \ 160; Por CALs de dispositivo) do relatório.
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- Método FetchReportPerDeviceEntries Serviços de Área de Trabalho Remota
- Método FetchReportPerDeviceEntries Serviços de Área de Trabalho Remota classe Win32_TSLicenseReport ,
- Win32_TSLicenseReport classe Serviços de Área de Trabalho Remota método FetchReportPerDeviceEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportPerDeviceEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3a5ef050002da069f7eda56352f204797cac521885248bc7e63dfd77f840f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737556"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportPerDeviceEntries da classe \_ Win32 TSLicenseReport

Recupera informações de licenças de acesso de cliente Serviços de Área de Trabalho Remota por dispositivo emitidas (CALs de RDS por dispositivo) do relatório.

## <a name="syntax"></a>Sintaxe


```mof
uint32 FetchReportPerDeviceEntries(
  [in]      uint32                              StartIndex,
  [in, out] uint32                              Count,
  [out]     Win32_TSLicenseReportPerDeviceEntry ReportPerDeviceEntries[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartIndex* \[ Em\]
</dt> <dd>

O índice da primeira entrada de relatório a ser recuperada. A primeira entrada de relatório tem um índice de zero.

</dd> <dt>

*Contagem* \[ in, out\]
</dt> <dd>

O número de entradas de relatório a recuperar do objeto de relatório. Um valor de zero indica que todas as entradas de relatório começando em *StartIndex* devem ser recuperadas. No retorno, contém o número de entradas na *matriz ReportPerDeviceEntries.*

</dd> <dt>

*ReportPerDeviceEntries* \[ out\]
</dt> <dd>

Uma matriz de [**classes \_ Win32 TSLicenseReportPerDeviceEntry**](win32-tslicensereportperdeviceentry.md) representa as entradas de licença recuperadas. O *parâmetro Count* contém o número de elementos nessa matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> </dl>

 

 





