---
description: O método CopyEx copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro FileName.
ms.assetid: e52c1a0f-e34c-4a61-9e54-ed172976cb61
ms.tgt_platform: multiple
title: Método CopyEx da classe CIM_DataFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60d2d0e6802aac62384a9d686831867d556cdb2c4a63630199c9989a5263188a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547476"
---
# <a name="copyex-method-of-the-cim_datafile-class"></a>Método CopyEx da classe CIM \_ DataFile

O **método CopyEx** copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo *parâmetro FileName.* Uma cópia não será suportada se ela exigir a substituição de um arquivo lógico existente. Esse método é uma versão estendida do método [**Copy**](copy-method-in-class-cim-datafile.md) e é herdado de [CIM \_ LogicalFile.](cim-logicalfile.md)

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FileName* \[ Em\]
</dt> <dd>

Nome totalmente qualificado do arquivo de destino (ou diretório).

Exemplo: "c: \\ temp \\ newdirectory"

</dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou. Esse parâmetro será **nulo se** o método for bem-sucedido.

</dd> <dt>

*StartFileName* \[ Em\]
</dt> <dd>

Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como um ponto de partida para esse método. Normalmente, o *parâmetro StartFileName* é o parâmetro *StopFileName* que especifica o arquivo (ou diretório) no qual ocorreu um erro da chamada de método anterior. Se esse parâmetro for **nulo,** a operação será executada no arquivo (ou diretório) especificado na [**chamada ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)

Se *StartFileName* for usado, *Recursive* também deverá ser definido como true.

</dd> <dt>

*Recursivo* \[ Em\]
</dt> <dd>

Se TRUE, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela [**instância do Cim \_ DataFile.**](cim-datafile.md) Para instâncias de arquivo, esse parâmetro é ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro. Para obter códigos de erro adicionais, [**consulte Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>


</dt> <dd>

0

Sucesso.

</dd> <dt>


</dt> <dd>

2

Acesso negado

</dd> <dt>


</dt> <dd>

8

Falha não especificada.

</dd> <dt>


</dt> <dd>

9

Objeto inválido.

</dd> <dt>


</dt> <dd>

10

O objeto já existe.

</dd> <dt>


</dt> <dd>

11

Sistema de arquivos não NTFS.

</dd> <dt>


</dt> <dd>

12

Plataforma não Windows.

</dd> <dt>


</dt> <dd>

13

A unidade não é a mesma.

</dd> <dt>


</dt> <dd>

14

O diretório não está vazio.

</dd> <dt>


</dt> <dd>

15

Violação de compartilhamento.

</dd> <dt>


</dt> <dd>

16

Arquivo inicial inválido.

</dd> <dt>


</dt> <dd>

17

Privilégio não mantido.

</dd> <dt>


</dt> <dd>

21

Parâmetro inválido.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **método CopyEx** no [**CIM \_ DataFile**](cim-datafile.md) é implementado pelo WMI.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[Tarefas WMI: Arquivos e Pastas](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Constantes de direitos de acesso de arquivo e diretório**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

