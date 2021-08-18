---
title: Método FetchReportFailedPerUserEntries da classe Win32_TSLicenseReport
description: Recupera detalhes de Serviços de Área de Trabalho Remota com falha por licenças de acesso para cliente por usuário (RDS \ 160; CALs por usuário) do relatório.
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método FetchReportFailedPerUserEntries
- Método FetchReportFailedPerUserEntries Serviços de Área de Trabalho Remota, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Serviços de Área de Trabalho Remota, método FetchReportFailedPerUserEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce4d78ff13ff58f7e80c1f177728ded24dc98588b0a0fb25c3976e9dcc19fdc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737626"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportFailedPerUserEntries da classe Win32 \_ TSLicenseReport

Recupera detalhes das licenças de acesso para cliente por usuário com falha Serviços de Área de Trabalho Remota (RDS CALs por usuário) do relatório.

## <a name="syntax"></a>Sintaxe


```mof
uint32 FetchReportFailedPerUserEntries(
  [in]      uint32                                  StartIndex,
  [in, out] uint32                                  Count,
  [out]     Win32_TSLicenseReportFailedPerUserEntry ReportFailedPerUserEntries[]
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

O número de entradas de relatório a serem recuperadas do objeto de relatório. Um valor de zero indica que todas as entradas de relatório começando em *startIndex* devem ser recuperadas. No retorno, contém o número de entradas na matriz *ReportFailedPerUserEntries* .

</dd> <dt>

*ReportFailedPerUserEntries* \[ fora\]
</dt> <dd>

Uma matriz de [**classes \_ TSLicenseReportFailedPerUserEntry do Win32**](win32-tslicensereportfailedperuserentry.md) que representam as entradas de licença recuperadas. O parâmetro *Count* contém o número de elementos nessa matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

 





