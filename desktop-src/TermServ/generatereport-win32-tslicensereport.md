---
title: Método GenerateReport da classe Win32_TSLicenseReport (GPMgmt. h)
description: O GenerateReport não está mais disponível para uso a partir do Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GenerateReport
- Método GenerateReport Serviços de Área de Trabalho Remota, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Serviços de Área de Trabalho Remota, método GenerateReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369783"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a>Método GenerateReport da classe Win32 \_ TSLicenseReport

\[O **GenerateReport** não está mais disponível para uso a partir do Windows Server 2012. Em vez disso, use [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]

Não há suporte para o método.

**Windows server 2008 R2 e Windows server 2008:** Gera um relatório de uso de licença por usuário atual no servidor de licença Área de Trabalho Remota.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Escopotype* \[ no\]
</dt> <dd>

Escopo do relatório de uso da licença. Ele pode ter os valores a seguir.

<dt>

1
</dt> <dd>

O relatório será gerado para todo o domínio.

</dd> <dt>

2
</dt> <dd>

O relatório será gerado para a unidade organizacional (UO) especificada no parâmetro *scopevalue* .

</dd> <dt>

3
</dt> <dd>

O relatório será gerado para todos os domínios confiáveis.

</dd> </dl> </dd> <dt>

*Escopovalue* \[ no\]
</dt> <dd>

Se o parâmetro *ScopeType* é 2, *ScopeType* especifica a UO para a qual o relatório será gerado. Você deve especificar *scopevalue* usando o formato **ou =**_OUName1_*_, ou =_*_OUName2_*_..._*.

</dd> <dt>

*Nome do arquivo* \[ fora\]
</dt> <dd>

O nome do arquivo do relatório gerado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o **WBEM \_ E \_ não \_ tem suporte**.

**Windows server 2008 R2 e Windows server 2008:** Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Esse é um método estático.

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Fim do suporte do cliente<br/>    | Nenhum compatível<br/>                                                                 |
| Fim do suporte do servidor<br/>    | Windows Server 2008 R2<br/>                                                         |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| parâmetro<br/>                   | <dl> <dt>GPMgmt. h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> </dl>

 

