---
title: Método FetchReportEntries da classe Win32_TSLicenseReport
description: Recupera detalhes de Serviços de Área de Trabalho Remota licenças de acesso para cliente por usuário (RDS \ 160; CALs por usuário) do relatório. Cada entrada representa um RDS \ 160; CAL por usuário que está em uso no momento.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método FetchReportEntries
- Método FetchReportEntries Serviços de Área de Trabalho Remota, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Serviços de Área de Trabalho Remota, método FetchReportEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc64c9591444307ba0519da02cf9c6f13d20252e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499731"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportEntries da classe Win32 \_ TSLicenseReport

Recupera detalhes de Serviços de Área de Trabalho Remota licenças de acesso para cliente por usuário (RDS CALs por usuário) do relatório. Cada entrada representa uma CAL RDS por usuário que está em uso no momento.

## <a name="syntax"></a>Sintaxe


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartIndex* \[ no\]
</dt> <dd>

Índice da primeira entrada de relatório a ser recebida. A primeira entrada de relatório tem um índice de zero.

</dd> <dt>

*Contagem* \[ de entrada, saída\]
</dt> <dd>

Número de entradas de relatório a serem recuperadas do objeto de relatório. Um valor de zero indica que todas as entradas de relatório começando em *startIndex* devem ser recuperadas. No retorno, contém o número de entradas na matriz *ReportEntries* .

</dd> <dt>

*ReportEntries* \[ fora\]
</dt> <dd>

Retorna uma matriz de [**classes \_ TSLicenseReportEntry do Win32**](win32-tslicensereportentry.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Um valor de **LSERVER \_ que \_ não \_ mais \_ dados** (0x4001) indica que não há mais entradas de relatório.

## <a name="remarks"></a>Comentários

Esse não é um método estático. Esse método deve ser chamado de um objeto de relatório de uso de licença por usuário.

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> </dl>

 

