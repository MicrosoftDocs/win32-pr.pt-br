---
description: Observação Em vez de usar essa função herdada, recomendamos que você use a API D3DDisassemble. Essa função – que desmonta um sombreador compilado em uma cadeia de caracteres de texto que contém instruções de assembly e registrar atribuições – não existe mais.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: Função D3DX10DisassembleShader (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: bd69b6dc2cede96e6ca07983195d202cfd248633f44a13fe1967393c446ca329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753216"
---
# <a name="d3dx10disassembleshader-function"></a>Função D3DX10DisassembleShader

> [!Note]  
> Em vez de usar essa função herdada, recomendamos que você use a API [**D3DDisassemble.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble)

 

Essa função – que desmonta um sombreador compilado em uma cadeia de caracteres de texto que contém instruções de assembly e registrar atribuições – não existe mais. Em vez disso, [**use D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pShader* \[ Em\]
</dt> <dd>

Tipo: **const \* void**

Um ponteiro para o [**sombreador compilado.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)

</dd> <dt>

*BytecodeLength* \[ Em\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

O tamanho de pShader.

</dd> <dt>

*EnableColorCode* \[ Em\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Inclua marcas HTML na saída para codificar a cor do resultado.

</dd> <dt>

*pComments* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

A cadeia de caracteres de comentário na parte superior do sombreador que identifica as constantes e as variáveis do sombreador.

</dd> <dt>

*ppDisassembly* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Endereço de um buffer (consulte [**Interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém o sombreador desmontado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 10 a seguir.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Esse texto retornado inclui um header com a versão do compilador HLSL usada para gerar esse objeto, comentários que descrevem o layout de memória dos buffers constantes usados pelo sombreador, assinaturas de entrada e saída e pontos de associação de recursos.

Aqui está um exemplo de desmontagem de um sombreador compilado. O exemplo supõe que você comece com um sombreador compilado (mostrado como *pVSBuf,* que pode ser exibido em [Exemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
