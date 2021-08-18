---
description: Método CompressEx da classe CIM_DataFile – usa a compactação NTFS para compactar o arquivo lógico (ou diretório) que é especificado no caminho do objeto. Esse método é herdado do \_ LogicalFile CIM.
ms.assetid: 553b6a90-d16c-4abb-9015-66fe8e1606f6
ms.tgt_platform: multiple
title: Método CompressEx da classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad63096e34283ae6ea763690045072b5d2e5579ce1f459bcc7c7bc92d671e0db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420154"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a>Método CompressEx da classe de \_ datafilefiles CIM

O método **CompressEx** usa a compactação NTFS para compactar o arquivo lógico (ou diretório) que é especificado no caminho do objeto. Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md). Esse método é uma versão estendida do método [**compress**](compress-method-in-class-cim-datafile.md) e é herdado de [CIM \_ LogicalFile](/windows/desktop/WmiSdk/calling-a-method).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StopFileName* \[ fora\]
</dt> <dd>

Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou. Esse parâmetro será nulo se o método tiver sucesso.

</dd> <dt>

*StartFileName* \[ no\]
</dt> <dd>

Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método. Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada de método anterior. Se esse parâmetro for nulo, a operação será executada no arquivo ou diretório especificado na chamada de **ExecMethod** .

Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.

</dd> <dt>

*Recursivo* \[ no\]
</dt> <dd>

Se **for true**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância de [**\_ arquivo**](cim-datafile.md) de arquivos CIM. Para instâncias de arquivo, esse parâmetro é ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Êxito.

</dd> <dt>

**2**
</dt> <dd>

Acesso negado

</dd> <dt>

**8**
</dt> <dd>

Falha não especificada.

</dd> <dt>

**9**
</dt> <dd>

Objeto inválido.

</dd> <dt>

**10**
</dt> <dd>

O objeto já existe.

</dd> <dt>

**11**
</dt> <dd>

Sistema de arquivos não NTFS.

</dd> <dt>

**12**
</dt> <dd>

Plataforma não Windows.

</dd> <dt>

**13**
</dt> <dd>

A unidade não é a mesma.

</dd> <dt>

**14**
</dt> <dd>

O diretório não está vazio.

</dd> <dt>

**15**
</dt> <dd>

Violação de compartilhamento.

</dd> <dt>

**16**
</dt> <dd>

Arquivo inicial inválido.

</dd> <dt>

**17**
</dt> <dd>

Privilégio não mantido.

</dd> <dt>

**Abril**
</dt> <dd>

Parâmetro inválido.

</dd> </dl>

## <a name="remarks"></a>Comentários

O método **CompressEx** no [**\_ arquivo CIM**](cim-datafile.md) é implementado pelo WMI.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DataFile de CIM \_](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[**DataFile de CIM \_**](cim-datafile.md)
</dt> <dt>

[Tarefas do WMI: arquivos e pastas](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Constantes de direitos de acesso de arquivo e diretório**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

