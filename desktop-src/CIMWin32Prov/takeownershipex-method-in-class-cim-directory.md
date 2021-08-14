---
description: Obtém a propriedade do arquivo de entrada de diretório lógico especificado no caminho do objeto. Esse método é uma versão estendida do método TakeOwnerShip e é herdado de CIM \_ LogicalFile.
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx da CIM_Directory classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5637e45c6dad7eec3f79ffd045a4a8d0dd3f3ba51ed5a60c09916c11802b1130
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119332776"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a>Método TakeOwnerShipEx da classe de diretório CIM \_

O **método TakeOwnerShipEx** obtém a propriedade do arquivo de entrada de diretório lógico especificado no caminho do objeto. Esse método é uma versão estendida do [**método TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) e é herdado de [**CIM \_ LogicalFile.**](cim-logicalfile.md) Se o arquivo lógico for um diretório, esse método atuará recursivamente, assumindo a propriedade de todos os arquivos e subdados que o diretório contém.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou. Esse parâmetro será nulo se o método for bem-sucedido.

</dd> <dt>

*StartFileName* \[ Em\]
</dt> <dd>

Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como um ponto de partida para esse método. Normalmente, esse parâmetro é o *parâmetro StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada de método anterior. Se esse parâmetro for nulo, a operação será executada no arquivo (ou diretório) especificado na [**chamada ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)

</dd> <dt>

*Recursivo* \[ Em\]
</dt> <dd>

Se **True**, o método será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância do [**\_ Diretório CIM.**](cim-directory.md) Para instâncias de arquivo, esse parâmetro é ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 em caso de êxito e qualquer outro número para indicar um erro.

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

A plataforma não é Windows.

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

Atualmente, esse método não é implementado pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="examples"></a>Exemplos

O código Visual Basic Script a seguir chama o **método TakeOwnerShipEx** para assumir a propriedade da pasta \\ temporária C: .


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



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

[Diretório \_ CIM](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[**Diretório \_ CIM**](cim-directory.md)
</dt> </dl>

 

