---
description: Método Copy da classe CIM_Directory – o método Copy copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.
ms.assetid: 71481cc8-9052-4c62-9c26-6887ea646ee1
ms.tgt_platform: multiple
title: Método Copy da classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb80c13ad25bac8a50764cd6e34127217e4476336af4690a519ba7adfc46948f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020674"
---
# <a name="copy-method-of-the-cim_directory-class"></a>Método Copy da classe de \_ diretório CIM

O método **Copy** copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada. Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária. Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do arquivo* \[ no\]
</dt> <dd>

Nome totalmente qualificado da cópia do arquivo de destino (ou diretório).

Exemplo: "c: \\ temp \\ newdirectory"

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor 0 em caso de êxito e qualquer outro número para indicar um erro.

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

[\_Diretório CIM](copy-method-in-class-cim-directory.md)
</dt> <dt>

[**\_Diretório CIM**](cim-directory.md)
</dt> </dl>

 

