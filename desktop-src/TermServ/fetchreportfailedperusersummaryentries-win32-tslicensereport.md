---
title: Método FetchReportFailedPerUserSummaryEntries da classe Win32_TSLicenseReport
description: Recupera informações de Resumo de falhas de Serviços de Área de Trabalho Remota por licenças de acesso para cliente por usuário (RDS \ 160; CALs por usuário) do relatório.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método FetchReportFailedPerUserSummaryEntries
- Método FetchReportFailedPerUserSummaryEntries Serviços de Área de Trabalho Remota, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Serviços de Área de Trabalho Remota, método FetchReportFailedPerUserSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219c2c854e04dabf8b5bfe0b5b70a07bbc3c57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759947"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportFailedPerUserSummaryEntries da classe Win32 \_ TSLicenseReport

Recupera informações resumidas de falhas de Serviços de Área de Trabalho Remota por licenças de acesso para cliente por usuário (RDS CALs por usuário) do relatório.

## <a name="syntax"></a>Sintaxe


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartIndex* \[ no\]
</dt> <dd>

O índice da primeira entrada de relatório a ser recuperada. A primeira entrada de relatório tem um índice de zero.

</dd> <dt>

*Contagem* \[ de entrada, saída\]
</dt> <dd>

O número de entradas de relatório a serem recuperadas do objeto de relatório. Um valor de zero indica que todas as entradas de relatório começando em *startIndex* devem ser recuperadas. No retorno, contém o número de entradas na matriz *ReportFailedPerUserSummaryEntries* .

</dd> <dt>

*ReportFailedPerUserSummaryEntries* \[ fora\]
</dt> <dd>

Uma matriz de [**classes \_ TSLicenseReportFailedPerUserSummaryEntry do Win32**](win32-tslicensereportfailedperusersummaryentry.md) que representam as entradas de licença recuperadas. O parâmetro *Count* contém o número de elementos nessa matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> </dl>

 

 





