---
description: Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método uncompact.
ms.assetid: 383475ba-77d4-4bfb-a241-9c37aa594a1e
ms.tgt_platform: multiple
title: Método UncompressEx da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c514939425625c15f3b683e4dc10bd5e05cb511
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646508"
---
# <a name="uncompressex-method-of-the-cim_logicalfile-class"></a>Método UncompressEx da classe de \_ LogicalFile CIM

O método **UncompressEx** descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método [**uncompact**](uncompress-method-in-class-cim-logicalfile.md) .

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StopFileName* \[ fora\]
</dt> <dd>

Nome do arquivo (ou diretório) em que o método falhou. Esse parâmetro será **nulo** se o método tiver sucesso.

</dd> <dt>

*StartFileName* \[ em, opcional\]
</dt> <dd>

Nome do arquivo filho (ou diretório) a ser usado como ponto de partida para o método. Normalmente, esse parâmetro é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior. Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Recursivo* \[ em, opcional\]
</dt> <dd>

Se **for true**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) . Para instâncias de arquivo, esse parâmetro é ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.

<dl> <dt>

**Êxito**
</dt> <dd>

0

Sucesso.

</dd> <dt>

**Acesso negado**
</dt> <dd>

2

Acesso negado.

</dd> <dt>

**Falha não especificada**
</dt> <dd>

8

Falha não especificada.

</dd> <dt>

**Objeto inválido**
</dt> <dd>

9

Objeto inválido.

</dd> <dt>

**O objeto já existe**
</dt> <dd>

10

O objeto já existe.

</dd> <dt>

**Sistema de arquivos não NTFS**
</dt> <dd>

11

Sistema de arquivos não NTFS.

</dd> <dt>

**Plataforma não NT/Windows 2000**
</dt> <dd>

12

Plataforma não Windows.

</dd> <dt>

**A unidade não é a mesma**
</dt> <dd>

13

A unidade não é a mesma.

</dd> <dt>

**Diretório não vazio**
</dt> <dd>

14

O diretório não está vazio.

</dd> <dt>

**Violação de compartilhamento**
</dt> <dd>

15

Violação de compartilhamento.

</dd> <dt>

**Arquivo de início inválido**
</dt> <dd>

16

Arquivo inicial inválido.

</dd> <dt>

**Privilégio não mantido**
</dt> <dd>

17

Privilégio não mantido.

</dd> <dt>

**Parâmetro inválido**
</dt> <dd>

21

Parâmetro inválido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Este método não está implementado no momento pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

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

[CIM \_ LogicalFile](uncompressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

