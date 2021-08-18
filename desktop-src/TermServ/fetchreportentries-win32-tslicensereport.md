---
title: Método FetchReportEntries da Win32_TSLicenseReport classe
description: Recupera detalhes de licenças Serviços de Área de Trabalho Remota acesso de cliente por usuário (RDS \ 160; Por CALs de usuário) do relatório. Cada entrada representa um RDS \ 160; Por CAL de usuário que está em uso no momento.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- Método FetchReportEntries Serviços de Área de Trabalho Remota
- Método FetchReportEntries Serviços de Área de Trabalho Remota , Win32_TSLicenseReport classe
- Win32_TSLicenseReport classe Serviços de Área de Trabalho Remota método FetchReportEntries
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
ms.openlocfilehash: e35c2af0578b0b130b5ef92bae5d374cc4ba2ba82c172689d00782e68b65c143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871725"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportEntries da classe Win32 \_ TSLicenseReport

Recupera detalhes de Serviços de Área de Trabalho Remota licenças de acesso de cliente por usuário (CALs de RDS por usuário) do relatório. Cada entrada representa uma CAL de RDS por usuário que está atualmente em uso.

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

*StartIndex* \[ Em\]
</dt> <dd>

Índice da primeira entrada de relatório a ser recebida. A primeira entrada de relatório tem um índice de zero.

</dd> <dt>

*Contagem* \[ in, out\]
</dt> <dd>

Número de entradas de relatório a recuperar do objeto de relatório. Um valor de zero indica que todas as entradas de relatório começando em *StartIndex* devem ser recuperadas. No retorno, contém o número de entradas na matriz *ReportEntries.*

</dd> <dt>

*Entradas de Relatório* \[ out\]
</dt> <dd>

Retorna uma matriz de [**classes \_ Win32 TSLicenseReportEntry.**](win32-tslicensereportentry.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Um valor de **LSERVER \_ I NO MORE \_ \_ \_ DATA** (0x4001) indica que não há mais entradas de relatório.

## <a name="remarks"></a>Comentários

Esse não é um método estático. Esse método deve ser chamado de um objeto de relatório de uso de licença por usuário.

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> </dl>

 

