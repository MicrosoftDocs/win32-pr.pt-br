---
description: Contém informações que identificam o adaptador.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: Estrutura de D3DADAPTER_IDENTIFIER9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: db4b25cb44b3b43b3b9754f241e2c505bdfedbc7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343391"
---
# <a name="d3dadapter_identifier9-structure"></a>\_Estrutura D3DADAPTER IDENTIFIER9

Contém informações que identificam o adaptador.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
  LARGE_INTEGER DriverVersion;
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a>Membros

<dl> <dt>

**Driver**
</dt> <dd>

Tipo: **Char**

</dd> <dd>

Usado para apresentação para o usuário. Isso não deve ser usado para identificar drivers específicos, pois muitas cadeias de caracteres diferentes podem ser associadas ao mesmo dispositivo e driver de fornecedores diferentes.

</dd> <dt>

**Descrição**
</dt> <dd>

Tipo: **Char**

</dd> <dd>

Usado para apresentação para o usuário.

</dd> <dt>

**DeviceName**
</dt> <dd>

Tipo: **Char**

</dd> <dd>

Nome do dispositivo para GDI.

</dd> <dt>

**DriverVersion**
</dt> <dd>

Tipo: **[ **\_ inteiro grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Identifique a versão do driver do Direct3D. É legal fazer menos de e maior que comparações no valor inteiro com sinal de 64 bits. No entanto, tome cuidado se você usar esse elemento para identificar drivers problemáticos. Em vez disso, você deve usar DeviceIdentifier. Consulte Observações.

</dd> <dt>

**DriverVersionLowPart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifique a versão do driver Direct3D. É legal fazer comparações < e > no valor inteiro com sinal de 64 bits. No entanto, tenha cuidado se você usar esse elemento para identificar drivers problemáticos. Em vez disso, você deve usar DeviceIdentifier. Consulte Observações.

</dd> <dt>

**DriverVersionHighPart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifique a versão do driver Direct3D. É legal fazer comparações < e > no valor inteiro com sinal de 64 bits. No entanto, tenha cuidado se você usar esse elemento para identificar drivers problemáticos. Em vez disso, você deve usar DeviceIdentifier. Consulte Observações.

</dd> <dt>

**Vendorid**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Pode ser usado para ajudar a identificar um conjunto de chip específico. Consulte este membro para identificar o fabricante. O valor pode ser zero se for desconhecido.

</dd> <dt>

**DeviceId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Pode ser usado para ajudar a identificar um conjunto de chip específico. Consulte este membro para identificar o tipo de conjunto de chip. O valor pode ser zero se for desconhecido.

</dd> <dt>

**SubSysId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Pode ser usado para ajudar a identificar um determinado conjunto de chips. Consulte este membro para identificar o subsistema, normalmente o quadro específico. O valor pode ser zero se for desconhecido.

</dd> <dt>

**Revisão**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Pode ser usado para ajudar a identificar um determinado conjunto de chips. Consulte este membro para identificar o nível de revisão do conjunto de chips. O valor pode ser zero se for desconhecido.

</dd> <dt>

**DeviceIdentifier**
</dt> <dd>

Tipo: **[ **GUID**](guid.md)**

</dd> <dd>

Pode ser consultado para verificar as alterações no driver e no conjunto de chips. Esse GUID é um identificador exclusivo para o par de drivers e conjuntos de chips. Consulte este membro para controlar as alterações no driver e no conjunto de chips para gerar um novo perfil para o subsistema de gráficos. O DeviceIdentifier também pode ser usado para identificar drivers problemáticos específicos.

</dd> <dt>

**WHQLLevel**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Usado para determinar o nível de validação do WHQL (Windows Hardware Quality Labs) para este driver e par de dispositivos. O DWORD é uma estrutura de data empacotada que define a data da versão do teste WHQL mais recente passado pelo driver. É legal executar < e > operações nesse valor. O exemplo a seguir ilustra o formato de data.



| Bits  |  Descrição                                             |
|-------|-----------------------------------------------|
| 31-16 | O ano, um número decimal de 1999 para cima. |
| 15-8  | O mês, um número decimal de 1 a 12.     |
| 7-0   | O dia, um número decimal de 1 a 31.       |



 

Os valores a seguir também são usados.



| Valor    |  Descrição                                                     |
|-----|-------------------------------------------------------|
| 0   | Não certificado.                                        |
| 1   | WHQL validado, mas nenhuma informação de data está disponível. |



 

Diferenças entre o Direct3D 9 e o Direct3D 9Ex:

Para Direct3D9Ex em execução no Windows Vista, Windows Server 2008, Windows 7 e Windows Server 2008 R2 (ou sistema operacional mais atual), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) retorna 1 para o nível WHQL sem verificar o status do driver.

</dd> </dl>

## <a name="remarks"></a>Comentários

O exemplo de pseudocódigo a seguir ilustra o formato de versão codificado nos membros DriverVersion, DriverVersionLowPart e DriverVersionHighPart.


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



Consulte o SDK da plataforma para obter mais informações sobre a macro HIWORD, a macro LOWORD e a estrutura \_ INTEGER GRANDE.

MAX \_ DEVICE \_ IDENTIFIER STRING é uma constante com a \_ definição a seguir.


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



Os membros VendorId, DeviceId, SubSysId e Revision podem ser usados em conjunto para identificar conjuntos de chip específicos. No entanto, use esses membros com cuidado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
